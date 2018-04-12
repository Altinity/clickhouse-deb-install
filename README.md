# clickhouse-deb-install

ClickHouse DEB packages installation from packagecloud.io

# Install Altinity packagecloud.io repo
```bash
curl -s https://packagecloud.io/install/repositories/Altinity/clickhouse/script.deb.sh | sudo bash
```

# Install GCC-7

ClickHouse for Debian required gcc-7 and glibc 2.27, which is distributed with gcc-7
Install `gcc-7`

Append in `/etc/apt/sources.list` entries for test packages. So far `gcc-7` is still a test package for debian

```bash
sudo bash -c 'echo "deb http://deb.debian.org/debian testing main" >> /etc/apt/sources.list'

```

Now install `gcc-7`

```bash
sudo apt-get update
sudo apt-get install -y gcc-7 g++-7
```

Now install `clickhouse`

```bash
sudo apt install 'clickhouse*'
```


And restart `ClickHouse` service

```bash
sudo /etc/init.d/clickhouse-server restart
```

