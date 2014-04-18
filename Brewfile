# Install command-line tools using Homebrew
# Usage: `brew bundle Brewfile`

# Make sure we’re using the latest Homebrew
update

# Upgrade any already-installed formulae
upgrade

# Install GNU core utilities (those that come with OS X are outdated)
# Don’t forget to add `$(brew --prefix coreutils)/libexec/gnubin` to `$PATH`.
install coreutils
# Install some other useful utilities like `sponge`
install moreutils
# Install GNU `find`, `locate`, `updatedb`, and `xargs`, `g`-prefixed
install findutils
# Install GNU `sed`, overwriting the built-in `sed`
install gnu-sed --default-names
# Install Bash 4
install bash

# Install wget with IRI support
install wget --enable-iri

# Install RingoJS and Narwhal
# Note that the order in which these are installed is important; see http://git.io/brew-narwhal-ringo.
install ringojs
install narwhal

# Install more recent versions of some OS X tools
install vim --override-system-vi
install homebrew/dupes/grep
install josegonzalez/homebrew-php/php55

# This formula didn’t work well last time I tried it:
#install homebrew/dupes/screen

# Install other useful binaries
install ack
install dnsmasq
#install exiv2
#?install foremost
install git
install imagemagick --with-webp
install lynx
install mysql
install nmap
install node
install phantomjs
install p7zip
install pigz
install pv
install rename
install rhino
install sqlmap
install tree
install webkit2png
install zopfli

install homebrew/versions/lua52

# MAMP setup
# MySQL
sudo mkdir /var/mysql
sudo ln -s /tmp/mysql.sock /var/mysql/mysql.sock
ln -sfv /usr/local/opt/mysql/*.plist ~/Library/LaunchAgents
launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mysql.plist
# Dnsmasq
cp /usr/local/opt/dnsmasq/dnsmasq.conf.example /usr/local/etc/dnsmasq.conf
sudo cp -fv /usr/local/opt/dnsmasq/*.plist /Library/LaunchDaemons
sudo launchctl load /Library/LaunchDaemons/homebrew.mxcl.dnsmasq.plist

# Remove outdated versions from the cellar
cleanup
