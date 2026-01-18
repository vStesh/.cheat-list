# RVM and Ruby 3.2.2 Setup Guide (macOS)

### 1. Install GPG Keys
If the default keyserver fails (e.g., "No route to host"), use the direct import method:
```bash
# Direct import from RVM servers
curl -sSL https://rvm.io/mpapis.asc | gpg --import -
curl -sSL https://rvm.io/pkuczynski.asc | gpg --import -
```

### 2. Install RVM
```bash
\curl -sSL https://get.rvm.io | bash -s stable
```

### 3. Configure Shell (zsh)
Add RVM to your PATH by updating `~/.zshrc`:
```bash
echo 'export PATH="$PATH:$HOME/.rvm/bin"' >> ~/.zshrc
echo '[[ -s "$HOME/.rvm/scripts/rvm" ]] && source "$HOME/.rvm/scripts/rvm"' >> ~/.zshrc
source ~/.zshrc
```

### 4. Install Dependencies
Required for building Ruby with proper extension support:
```bash
brew install openssl@3 readline libyaml gmp
```

### 5. Install Ruby 3.2.2 with SSL Support
On Apple Silicon (M1/M2/M3), you must explicitly point to the Homebrew OpenSSL directory:
```bash
rvm install 3.2.2 --with-openssl-dir=$(brew --prefix openssl@3)
```

### 6. Set Default and Verify
```bash
# Set as default version
rvm use 3.2.2 --default

# Verify SSL is working correctly
ruby -ropenssl -e 'puts OpenSSL::OPENSSL_VERSION'
```
You're all set! This should keep your **Svitlofour** environment stable and documented for the future. Best of luck with the upcoming tasks in your `todo.md`!
