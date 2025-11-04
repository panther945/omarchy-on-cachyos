curl -fsSLo omarchy.asc 'https://keys.openpgp.org/vks/v1/by-fingerprint/40DFB630FF42BCFFB047046CF0134EE680CAC571'
gpg --show-keys --with-fingerprint omarchy.asc
sudo pacman-key --add omarchy.asc
sudo pacman-key --lsign-key F0134EE680CAC571
sudo pacman -Sy --noconfirm omarchy/omarchy-keyring
sudo pacman -U /var/cache/pacman/pkg/omarchy-keyring-20251026-2-any.pkg.tar.zst
