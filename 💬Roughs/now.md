watch -n 1 "grep MHz /proc/cpuinfo"
systemctl list-units --type=service | grep -E "power-profiles-daemon|tlp"
watch -n 2 sensors
sensors
sudo sensors-detect
sudo dnf install lm_sensors