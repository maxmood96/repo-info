## `chronograf:latest`

```console
$ docker pull chronograf@sha256:4a59c624580fde12aea45b2581e31bacb2c44310ba6ed2c07c6b86685a66ddcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:ff002113190bcfa0895d33a1e556f14f988b8d5c6f3bdaa0f3b365caa5239306
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70162782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e2dabfc384c5ecac92a12c7094c5886958be332553ad78a704f99f260d8b70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:09:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 23:10:16 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Tue, 04 Aug 2020 23:10:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 23:10:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 23:10:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 23:10:27 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 23:10:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 23:10:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 23:10:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 23:10:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28ec7a64ff33e918060654b47546b5cdaf7dea07fbc8d402fd30ce81f3724e`  
		Last Modified: Tue, 04 Aug 2020 23:10:42 GMT  
		Size: 4.5 MB (4504564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194fb287e3894a502d48edcd1a3e242ad4b78896063c231d7e57c00cf5756d3`  
		Last Modified: Tue, 04 Aug 2020 23:11:11 GMT  
		Size: 43.1 MB (43111548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a29f3af93d5cafc0f26341e8971e405c1f0bd9b483c20b8a1973ff3f932e09e`  
		Last Modified: Tue, 04 Aug 2020 23:11:03 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66974d2173ee70a96e2cc67705456ead5c5f0d1e622c0088c56d7fe5bbfd3853`  
		Last Modified: Tue, 04 Aug 2020 23:11:03 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fe0d3f8249dda31eb3cfb56d071dad03c68fd535019d06f13f59175266a2db`  
		Last Modified: Tue, 04 Aug 2020 23:11:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c0803f5c98a9b606fea7ea6fa6fb50a2bc93750996bc83ffb304c47f528ad71c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63563753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f9b03033028bf7afdee09c44e3a2f5ca551e4e125528907c13098da0d98858`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:30 GMT
ADD file:3d69e3d8fb19d3a9c5fc738b4c9b3c436f9ba10b16c057523360b3443dcd7570 in / 
# Tue, 04 Aug 2020 05:01:32 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:40:09 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 08:44:50 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Tue, 04 Aug 2020 08:45:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 08:45:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 08:45:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 08:45:22 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 08:45:22 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 08:45:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 08:45:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 08:45:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b33d4edf196b4a005f13932d074987a85eb6c927dc64b40989598b3ade8ebc5c`  
		Last Modified: Tue, 04 Aug 2020 05:09:01 GMT  
		Size: 19.3 MB (19304611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb933ad4bb85672991fffc11bb98b3d11d98ccd0523793e0699c1eb81ca6817e`  
		Last Modified: Tue, 04 Aug 2020 08:45:40 GMT  
		Size: 3.9 MB (3878320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56d04542cfbbb40ecceb3fb0857d765f0e9907bf4600635efb17582d63075af`  
		Last Modified: Tue, 04 Aug 2020 08:46:24 GMT  
		Size: 40.4 MB (40356413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc095732d5a67cce2400ab2414f1df138953b3f3dced02f04ef888cf7bca469`  
		Last Modified: Tue, 04 Aug 2020 08:46:13 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd518336b8728bf95dafdf81b66d9663cbea4d2f4c704d43ae4c87a67e08f06`  
		Last Modified: Tue, 04 Aug 2020 08:46:14 GMT  
		Size: 11.9 KB (11915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5247c0d8a61cdbdcb822b8b41db097f237b43fcef962c21317e43f883533ec1d`  
		Last Modified: Tue, 04 Aug 2020 08:46:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8eb0ff0b6d5d5498c86a78cbb270d24c86932ea242344d0b4b44e6143aefa84f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64684179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bc2d4a382fd8af58b27236da7aa64deb8b7fae272f10a79e2e3f91dd8e17a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 04 Aug 2020 07:00:02 GMT
ADD file:448eac8822629a9f212483d0e6123c797105b2ec368648e6f259b7d4cb83e0a1 in / 
# Tue, 04 Aug 2020 07:00:04 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 12:07:36 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 04 Aug 2020 12:08:44 GMT
ENV CHRONOGRAF_VERSION=1.8.4
# Tue, 04 Aug 2020 12:09:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 04 Aug 2020 12:09:04 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 04 Aug 2020 12:09:04 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 04 Aug 2020 12:09:05 GMT
EXPOSE 8888
# Tue, 04 Aug 2020 12:09:06 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Aug 2020 12:09:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 04 Aug 2020 12:09:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Aug 2020 12:09:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5984ce78d2759fcb147a7641f941b59e71e8c9f82aa5cb0e3d511c74c876a7e3`  
		Last Modified: Tue, 04 Aug 2020 07:06:31 GMT  
		Size: 20.4 MB (20377078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90498816ec3109a4a198e68a2e2d8566007ec9adc990d0cf643e17e587b408c`  
		Last Modified: Tue, 04 Aug 2020 12:09:21 GMT  
		Size: 4.1 MB (4081172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a49ca7891d76d2c35a5f376b7e56da548787d85c98b5ca929cdc944e43f00a6`  
		Last Modified: Tue, 04 Aug 2020 12:10:00 GMT  
		Size: 40.2 MB (40201536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787df7936b8ce5e1cd1e0e7cdbec1871ebf7e2ed85091d44ae2c5ede64af0ae3`  
		Last Modified: Tue, 04 Aug 2020 12:09:49 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d0a36509bb6778681565d6b9a5fbe7abb75738566870f66d0ac4a84e9d7831`  
		Last Modified: Tue, 04 Aug 2020 12:09:48 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a340602e108459595de3c4067bc0ddcbdf7a651d4790808865c0ca79a807c16a`  
		Last Modified: Tue, 04 Aug 2020 12:09:49 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
