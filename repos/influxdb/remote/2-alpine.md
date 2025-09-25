## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:fa166d3bdf6beeecf57791b70e558f6ef54e1e6cea95fb7728b45314bc48543b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d76a12db18d7b6e85c3bf97b9627d2043eac00a226367a71789aa4f511b2e675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78685978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1ccd747e4a1c0cfefc72d84b8878fd0133be8c5235727262a387f7c717437b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bee215043e4b9c592d3270a4f9ca98f743ad5efe2f15d29853608a33f501e9e`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd831899112efbf1818c7a1391b355b858f0978cd23d43c7301b385e94bb8fee`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 9.8 MB (9783483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95fb2184026d4eaa8b66c5dd24e1704f9b8656617244f9830dd08887fcd1c0c`  
		Last Modified: Wed, 24 Sep 2025 20:42:10 GMT  
		Size: 5.8 MB (5790447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b6d057364a9b4e36e9823da94eaf8835e9bac3b077c62a40c181b00530cdfa`  
		Last Modified: Wed, 24 Sep 2025 20:42:09 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edba18fd6c1832982b6768f2002eb35d3cf6c674c66c3250319a5de66db7415f`  
		Last Modified: Wed, 24 Sep 2025 20:42:15 GMT  
		Size: 48.0 MB (48017164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7edbd54c33d4091fc7334eb38238f440a45590e52b46baf71b46dd441a50ca`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3a4cfc59e5f76d849da88e7e676f8f42c75ea2fea9a6aa92ed3a2ea7a0b405`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7c6ec75ef0cf8c7cf00e47fc3b0650c76931084ae3b046ef3dfeb076c1f719`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92892ed38d0c82365147f5ff91c9b9018cf22b8a78c94d836c2c98259200b9e5`  
		Last Modified: Wed, 24 Sep 2025 20:42:12 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:da75c82cd2a446f08e03c0f1f2436f8078f27140db4413a43c3f36b73ff7bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **940.8 KB (940817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82968150aefd76734cd63972f5c9bb47ad207190dc4e58e3b34ff0ce3e584987`

```dockerfile
```

-	Layers:
	-	`sha256:ac04216069aed10e6fcf7796fc4b9979609d5f75599ec854456b1cade370bf2b`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 909.9 KB (909854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86c9d7656a12cb47dd5db65e1dfe6517aa607a0480a92ae559be75c02b87fffd`  
		Last Modified: Thu, 25 Sep 2025 02:22:10 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json
