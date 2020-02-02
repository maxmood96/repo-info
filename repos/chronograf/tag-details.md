<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.5`](#chronograf15)
-	[`chronograf:1.5.0`](#chronograf150)
-	[`chronograf:1.5.0.1`](#chronograf1501)
-	[`chronograf:1.5.0.1-alpine`](#chronograf1501-alpine)
-	[`chronograf:1.5.0-alpine`](#chronograf150-alpine)
-	[`chronograf:1.5-alpine`](#chronograf15-alpine)
-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7.16`](#chronograf1716)
-	[`chronograf:1.7.16-alpine`](#chronograf1716-alpine)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.5`

```console
$ docker pull chronograf@sha256:c2a9cab7fb4c4dad69b501a4e9fe168c9907d50ccf620763c74afe41ecdfb6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.5` - linux; amd64

```console
$ docker pull chronograf@sha256:dc3692e914b161e9445a769ec6aa0da4c0ec9d3fe7c43a134f9f84697199efa4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49107989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c8c886a40c65cd9e9c457f23f2018c28b4d782526f019d826bbed32341fe12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:48:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 00:48:29 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sun, 02 Feb 2020 00:48:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 00:48:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 02 Feb 2020 00:48:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 02 Feb 2020 00:48:40 GMT
EXPOSE 8888
# Sun, 02 Feb 2020 00:48:40 GMT
VOLUME [/var/lib/chronograf]
# Sun, 02 Feb 2020 00:48:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 02 Feb 2020 00:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 00:48:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af64bbf8137f9e6bd074ef982a1129016ddcbe37866e214ea199a7f9f105be`  
		Last Modified: Sun, 02 Feb 2020 00:49:37 GMT  
		Size: 4.5 MB (4503576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda6f8ed64c12a935c7393ed0468f070caae742cb45d695ca17f21af7d2d75de`  
		Last Modified: Sun, 02 Feb 2020 00:49:42 GMT  
		Size: 22.1 MB (22055303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e40c1577c4798a4c1ad5b73e4a1f8af41332685de3d0400f2fe5e15da2d775`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33737f7bb5041da5766a7d62ac90fb4e550bb454bd0a8b7ce5f764cee87fddd2`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc023ea106a4a2f0ea62feb5be66d829b32ff38bd1069376ad06248702560a68`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:48e5f3bfc797a31a7b959a7cd5f6cdc9a70ead3a321679c63c5e222ba0c07aa8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43675563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8905d696829c0a9e9332df36c997529c9ee75d28a5491a50a907f2f0cb0f13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:41:54 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sat, 01 Feb 2020 18:42:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:42:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:42:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:42:21 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:42:21 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:42:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:42:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4cca9d32e71087eece3066e9a90d8a2880b7a6fcdebed0b49c59caee7ac1a0`  
		Last Modified: Sat, 01 Feb 2020 18:44:02 GMT  
		Size: 20.5 MB (20462160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978137bb3c3aab475d5da2e3059e3d367ab9edd1cfd69d44c82d1eca6efe0a97`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7e84dbe18cd8e4ee93aa6ea27cc76c5826931d9545de1a0b3d8243cbd5ab38`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b54a8b42a4813bb02b415f462ce06958325f17676fb73688c2b2a6324a620aa`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:62bd486bc97f4d427c454d26d2ba43dd2d3628aae9c36038920c85a37f6a5d75
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45160556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bd077e24452da8a7a289f916462b43dff71317349dc82a6baf85d19ce5f4a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:53:13 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sat, 01 Feb 2020 17:53:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:53:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:53:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:53:36 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:53:37 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:53:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:53:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:53:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7037338107384d9532ad3dd496de8351467db41556637a6fb719a54e0f8779b`  
		Last Modified: Sat, 01 Feb 2020 17:55:33 GMT  
		Size: 20.7 MB (20669519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f76a1a5c591d0b7ccfb207c5913118ca889892c6c839dab3e5d3e1c0517cbf`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4355f1b4fb395e5c495f7ac55ed9cf8e914da8ea1e6cea8dc4829682a4cc65e`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b274e87fd3a3a96b138f95b37f91a5e1eee12c2eb6fd5ad0709c46c2172ce5be`  
		Last Modified: Sat, 01 Feb 2020 17:55:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.5.0`

```console
$ docker pull chronograf@sha256:c2a9cab7fb4c4dad69b501a4e9fe168c9907d50ccf620763c74afe41ecdfb6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.5.0` - linux; amd64

```console
$ docker pull chronograf@sha256:dc3692e914b161e9445a769ec6aa0da4c0ec9d3fe7c43a134f9f84697199efa4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49107989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c8c886a40c65cd9e9c457f23f2018c28b4d782526f019d826bbed32341fe12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:48:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 00:48:29 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sun, 02 Feb 2020 00:48:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 00:48:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 02 Feb 2020 00:48:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 02 Feb 2020 00:48:40 GMT
EXPOSE 8888
# Sun, 02 Feb 2020 00:48:40 GMT
VOLUME [/var/lib/chronograf]
# Sun, 02 Feb 2020 00:48:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 02 Feb 2020 00:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 00:48:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af64bbf8137f9e6bd074ef982a1129016ddcbe37866e214ea199a7f9f105be`  
		Last Modified: Sun, 02 Feb 2020 00:49:37 GMT  
		Size: 4.5 MB (4503576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda6f8ed64c12a935c7393ed0468f070caae742cb45d695ca17f21af7d2d75de`  
		Last Modified: Sun, 02 Feb 2020 00:49:42 GMT  
		Size: 22.1 MB (22055303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e40c1577c4798a4c1ad5b73e4a1f8af41332685de3d0400f2fe5e15da2d775`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33737f7bb5041da5766a7d62ac90fb4e550bb454bd0a8b7ce5f764cee87fddd2`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc023ea106a4a2f0ea62feb5be66d829b32ff38bd1069376ad06248702560a68`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.5.0` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:48e5f3bfc797a31a7b959a7cd5f6cdc9a70ead3a321679c63c5e222ba0c07aa8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43675563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8905d696829c0a9e9332df36c997529c9ee75d28a5491a50a907f2f0cb0f13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:41:54 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sat, 01 Feb 2020 18:42:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:42:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:42:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:42:21 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:42:21 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:42:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:42:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4cca9d32e71087eece3066e9a90d8a2880b7a6fcdebed0b49c59caee7ac1a0`  
		Last Modified: Sat, 01 Feb 2020 18:44:02 GMT  
		Size: 20.5 MB (20462160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978137bb3c3aab475d5da2e3059e3d367ab9edd1cfd69d44c82d1eca6efe0a97`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7e84dbe18cd8e4ee93aa6ea27cc76c5826931d9545de1a0b3d8243cbd5ab38`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b54a8b42a4813bb02b415f462ce06958325f17676fb73688c2b2a6324a620aa`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.5.0` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:62bd486bc97f4d427c454d26d2ba43dd2d3628aae9c36038920c85a37f6a5d75
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45160556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bd077e24452da8a7a289f916462b43dff71317349dc82a6baf85d19ce5f4a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:53:13 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sat, 01 Feb 2020 17:53:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:53:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:53:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:53:36 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:53:37 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:53:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:53:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:53:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7037338107384d9532ad3dd496de8351467db41556637a6fb719a54e0f8779b`  
		Last Modified: Sat, 01 Feb 2020 17:55:33 GMT  
		Size: 20.7 MB (20669519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f76a1a5c591d0b7ccfb207c5913118ca889892c6c839dab3e5d3e1c0517cbf`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4355f1b4fb395e5c495f7ac55ed9cf8e914da8ea1e6cea8dc4829682a4cc65e`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b274e87fd3a3a96b138f95b37f91a5e1eee12c2eb6fd5ad0709c46c2172ce5be`  
		Last Modified: Sat, 01 Feb 2020 17:55:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.5.0.1`

```console
$ docker pull chronograf@sha256:c2a9cab7fb4c4dad69b501a4e9fe168c9907d50ccf620763c74afe41ecdfb6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.5.0.1` - linux; amd64

```console
$ docker pull chronograf@sha256:dc3692e914b161e9445a769ec6aa0da4c0ec9d3fe7c43a134f9f84697199efa4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49107989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c8c886a40c65cd9e9c457f23f2018c28b4d782526f019d826bbed32341fe12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:48:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 00:48:29 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sun, 02 Feb 2020 00:48:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 00:48:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 02 Feb 2020 00:48:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 02 Feb 2020 00:48:40 GMT
EXPOSE 8888
# Sun, 02 Feb 2020 00:48:40 GMT
VOLUME [/var/lib/chronograf]
# Sun, 02 Feb 2020 00:48:41 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 02 Feb 2020 00:48:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 00:48:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af64bbf8137f9e6bd074ef982a1129016ddcbe37866e214ea199a7f9f105be`  
		Last Modified: Sun, 02 Feb 2020 00:49:37 GMT  
		Size: 4.5 MB (4503576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda6f8ed64c12a935c7393ed0468f070caae742cb45d695ca17f21af7d2d75de`  
		Last Modified: Sun, 02 Feb 2020 00:49:42 GMT  
		Size: 22.1 MB (22055303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e40c1577c4798a4c1ad5b73e4a1f8af41332685de3d0400f2fe5e15da2d775`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33737f7bb5041da5766a7d62ac90fb4e550bb454bd0a8b7ce5f764cee87fddd2`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc023ea106a4a2f0ea62feb5be66d829b32ff38bd1069376ad06248702560a68`  
		Last Modified: Sun, 02 Feb 2020 00:49:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.5.0.1` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:48e5f3bfc797a31a7b959a7cd5f6cdc9a70ead3a321679c63c5e222ba0c07aa8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43675563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8905d696829c0a9e9332df36c997529c9ee75d28a5491a50a907f2f0cb0f13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:41:54 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sat, 01 Feb 2020 18:42:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:42:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:42:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:42:21 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:42:21 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:42:22 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:42:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:42:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4cca9d32e71087eece3066e9a90d8a2880b7a6fcdebed0b49c59caee7ac1a0`  
		Last Modified: Sat, 01 Feb 2020 18:44:02 GMT  
		Size: 20.5 MB (20462160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978137bb3c3aab475d5da2e3059e3d367ab9edd1cfd69d44c82d1eca6efe0a97`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7e84dbe18cd8e4ee93aa6ea27cc76c5826931d9545de1a0b3d8243cbd5ab38`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b54a8b42a4813bb02b415f462ce06958325f17676fb73688c2b2a6324a620aa`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.5.0.1` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:62bd486bc97f4d427c454d26d2ba43dd2d3628aae9c36038920c85a37f6a5d75
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45160556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bd077e24452da8a7a289f916462b43dff71317349dc82a6baf85d19ce5f4a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:53:13 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Sat, 01 Feb 2020 17:53:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:53:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:53:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:53:36 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:53:37 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:53:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:53:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:53:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7037338107384d9532ad3dd496de8351467db41556637a6fb719a54e0f8779b`  
		Last Modified: Sat, 01 Feb 2020 17:55:33 GMT  
		Size: 20.7 MB (20669519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f76a1a5c591d0b7ccfb207c5913118ca889892c6c839dab3e5d3e1c0517cbf`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4355f1b4fb395e5c495f7ac55ed9cf8e914da8ea1e6cea8dc4829682a4cc65e`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b274e87fd3a3a96b138f95b37f91a5e1eee12c2eb6fd5ad0709c46c2172ce5be`  
		Last Modified: Sat, 01 Feb 2020 17:55:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.5.0.1-alpine`

```console
$ docker pull chronograf@sha256:96a8c2862d12647b69e69ea708919c174467a33bf9c4094c47c1c38b281d1362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.5.0.1-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f0e24b5af705a70ee5ec30f0ef3d899558ba84e9e0e28b6533eab0116a18447c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14714603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbefd794b199d2e4334ff284913c3c11d573a264dbe2d966c56058ae41f057f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:07 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Fri, 24 Jan 2020 06:18:11 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:11 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:12 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:12 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3b752cacd2c99d068949a8fa2863231a37be97894ff204e1aac95a3db46362`  
		Last Modified: Fri, 24 Jan 2020 06:19:00 GMT  
		Size: 11.6 MB (11624021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fa17657ce08f2051045c15e221d3a3d394406a34c5929e0f38043fab1708dc`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1033b1186465e211fd59c1374233b0b6f8f03db586c35e2ea6f9a4566fdf9d9`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411475a71eceec1dad8e44acb6a43adcffe4ed4c30aa9a0e952204231f9a9a01`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.5.0-alpine`

```console
$ docker pull chronograf@sha256:96a8c2862d12647b69e69ea708919c174467a33bf9c4094c47c1c38b281d1362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.5.0-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f0e24b5af705a70ee5ec30f0ef3d899558ba84e9e0e28b6533eab0116a18447c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14714603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbefd794b199d2e4334ff284913c3c11d573a264dbe2d966c56058ae41f057f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:07 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Fri, 24 Jan 2020 06:18:11 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:11 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:12 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:12 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3b752cacd2c99d068949a8fa2863231a37be97894ff204e1aac95a3db46362`  
		Last Modified: Fri, 24 Jan 2020 06:19:00 GMT  
		Size: 11.6 MB (11624021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fa17657ce08f2051045c15e221d3a3d394406a34c5929e0f38043fab1708dc`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1033b1186465e211fd59c1374233b0b6f8f03db586c35e2ea6f9a4566fdf9d9`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411475a71eceec1dad8e44acb6a43adcffe4ed4c30aa9a0e952204231f9a9a01`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.5-alpine`

```console
$ docker pull chronograf@sha256:96a8c2862d12647b69e69ea708919c174467a33bf9c4094c47c1c38b281d1362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f0e24b5af705a70ee5ec30f0ef3d899558ba84e9e0e28b6533eab0116a18447c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14714603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbefd794b199d2e4334ff284913c3c11d573a264dbe2d966c56058ae41f057f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:07 GMT
ENV CHRONOGRAF_VERSION=1.5.0.1
# Fri, 24 Jan 2020 06:18:11 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:11 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:11 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:12 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:12 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:12 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3b752cacd2c99d068949a8fa2863231a37be97894ff204e1aac95a3db46362`  
		Last Modified: Fri, 24 Jan 2020 06:19:00 GMT  
		Size: 11.6 MB (11624021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fa17657ce08f2051045c15e221d3a3d394406a34c5929e0f38043fab1708dc`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1033b1186465e211fd59c1374233b0b6f8f03db586c35e2ea6f9a4566fdf9d9`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411475a71eceec1dad8e44acb6a43adcffe4ed4c30aa9a0e952204231f9a9a01`  
		Last Modified: Fri, 24 Jan 2020 06:18:53 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:63a27d7f7e853830238409bacdd2ef0cb0e51d8318569c5e4e41e2e39be2898f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:c6ee8805c52b276decaa0ccfc5dfb8cfa482b12a3118258a360ca1c8bc9baf10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49152239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f65ce46694baa3f9c8dc84de937fd70194c371b2b5865cfabb28f4b028fd7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:48:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 00:48:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sun, 02 Feb 2020 00:48:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 00:49:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 02 Feb 2020 00:49:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 02 Feb 2020 00:49:00 GMT
EXPOSE 8888
# Sun, 02 Feb 2020 00:49:00 GMT
VOLUME [/var/lib/chronograf]
# Sun, 02 Feb 2020 00:49:01 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 02 Feb 2020 00:49:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 00:49:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af64bbf8137f9e6bd074ef982a1129016ddcbe37866e214ea199a7f9f105be`  
		Last Modified: Sun, 02 Feb 2020 00:49:37 GMT  
		Size: 4.5 MB (4503576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c940174a8deee1585322a1f8864e9c25fa7bfc8cfbbd57abb97389557b01b2a9`  
		Last Modified: Sun, 02 Feb 2020 00:49:50 GMT  
		Size: 22.1 MB (22099556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285a76358d84ef34dbf92f264a995ef72e80d2fc02b0049e3b8011568222d52`  
		Last Modified: Sun, 02 Feb 2020 00:49:46 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54c6627078cb6480ce68f8ed6018c52c480b8385d42ddb1c92825dd94607a26`  
		Last Modified: Sun, 02 Feb 2020 00:49:46 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107efddf4f0134e81a3f8c569f4c1973437e6927ab0256d9fa9a49c8be88728`  
		Last Modified: Sun, 02 Feb 2020 00:49:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8933c7f69cfed637f88a6199566ff0eec664af3a15fb8848035d54db61585107
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43738788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c092ad43a8a23df48b4a3945db46e0fbc871126b09f3899014711fba4c672b16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:42:34 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 01 Feb 2020 18:42:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:43:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:43:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:43:03 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:43:04 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:43:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:43:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:43:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813708d046172f8bc48e8a5fc748bbac45109ed1927cf338f80ecc4ded6b41b1`  
		Last Modified: Sat, 01 Feb 2020 18:44:16 GMT  
		Size: 20.5 MB (20525386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc883eb66a988bf75e7da78b67f43241e5b64601c0c386c073cdc14d6c6b905`  
		Last Modified: Sat, 01 Feb 2020 18:44:09 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840db23d86531d9141cd3a7bdc0ba47c4a39372d6da0d036595dc9560756f282`  
		Last Modified: Sat, 01 Feb 2020 18:44:09 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ecde31cd6d2d26ca60f5c6e201424231658bdf8978fd0ea7afa2f962c4637`  
		Last Modified: Sat, 01 Feb 2020 18:44:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:dbbaeb1f36ef739ac8fda8d567a7e53baf1e66a1c147325a94899f110ab12953
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45224524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3eabb311f8271524315b6ab4cf8902e7dd91f966401fc6b455fc002faebf51`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:53:44 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 01 Feb 2020 17:54:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:54:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:54:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:54:08 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:54:09 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:54:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:54:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:54:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876f5daf2cc33e4894ca19a921b7d0a503e572652257f740f1d76844f7d5df3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:46 GMT  
		Size: 20.7 MB (20733495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6b09b143d0dd218aa615163e44bbdb918f7307c20959c8f90ab3848900acec`  
		Last Modified: Sat, 01 Feb 2020 17:55:39 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b35d9822b7da97b03f68573238e5c0b9a484eaf8b352b71bd5db99dc8df7c2`  
		Last Modified: Sat, 01 Feb 2020 17:55:39 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1475e2d19f52d98172917c76764e2976b8b028af977665dea09c24ca05d219b4`  
		Last Modified: Sat, 01 Feb 2020 17:55:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:63a27d7f7e853830238409bacdd2ef0cb0e51d8318569c5e4e41e2e39be2898f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:c6ee8805c52b276decaa0ccfc5dfb8cfa482b12a3118258a360ca1c8bc9baf10
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49152239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f65ce46694baa3f9c8dc84de937fd70194c371b2b5865cfabb28f4b028fd7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:48:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 00:48:49 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sun, 02 Feb 2020 00:48:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 00:49:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 02 Feb 2020 00:49:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 02 Feb 2020 00:49:00 GMT
EXPOSE 8888
# Sun, 02 Feb 2020 00:49:00 GMT
VOLUME [/var/lib/chronograf]
# Sun, 02 Feb 2020 00:49:01 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 02 Feb 2020 00:49:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 00:49:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af64bbf8137f9e6bd074ef982a1129016ddcbe37866e214ea199a7f9f105be`  
		Last Modified: Sun, 02 Feb 2020 00:49:37 GMT  
		Size: 4.5 MB (4503576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c940174a8deee1585322a1f8864e9c25fa7bfc8cfbbd57abb97389557b01b2a9`  
		Last Modified: Sun, 02 Feb 2020 00:49:50 GMT  
		Size: 22.1 MB (22099556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285a76358d84ef34dbf92f264a995ef72e80d2fc02b0049e3b8011568222d52`  
		Last Modified: Sun, 02 Feb 2020 00:49:46 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54c6627078cb6480ce68f8ed6018c52c480b8385d42ddb1c92825dd94607a26`  
		Last Modified: Sun, 02 Feb 2020 00:49:46 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107efddf4f0134e81a3f8c569f4c1973437e6927ab0256d9fa9a49c8be88728`  
		Last Modified: Sun, 02 Feb 2020 00:49:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:8933c7f69cfed637f88a6199566ff0eec664af3a15fb8848035d54db61585107
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43738788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c092ad43a8a23df48b4a3945db46e0fbc871126b09f3899014711fba4c672b16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:42:34 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 01 Feb 2020 18:42:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:43:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:43:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:43:03 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:43:04 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:43:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:43:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:43:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813708d046172f8bc48e8a5fc748bbac45109ed1927cf338f80ecc4ded6b41b1`  
		Last Modified: Sat, 01 Feb 2020 18:44:16 GMT  
		Size: 20.5 MB (20525386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc883eb66a988bf75e7da78b67f43241e5b64601c0c386c073cdc14d6c6b905`  
		Last Modified: Sat, 01 Feb 2020 18:44:09 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840db23d86531d9141cd3a7bdc0ba47c4a39372d6da0d036595dc9560756f282`  
		Last Modified: Sat, 01 Feb 2020 18:44:09 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083ecde31cd6d2d26ca60f5c6e201424231658bdf8978fd0ea7afa2f962c4637`  
		Last Modified: Sat, 01 Feb 2020 18:44:09 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:dbbaeb1f36ef739ac8fda8d567a7e53baf1e66a1c147325a94899f110ab12953
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45224524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3eabb311f8271524315b6ab4cf8902e7dd91f966401fc6b455fc002faebf51`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:53:44 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Sat, 01 Feb 2020 17:54:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:54:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:54:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:54:08 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:54:09 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:54:10 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:54:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:54:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876f5daf2cc33e4894ca19a921b7d0a503e572652257f740f1d76844f7d5df3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:46 GMT  
		Size: 20.7 MB (20733495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6b09b143d0dd218aa615163e44bbdb918f7307c20959c8f90ab3848900acec`  
		Last Modified: Sat, 01 Feb 2020 17:55:39 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b35d9822b7da97b03f68573238e5c0b9a484eaf8b352b71bd5db99dc8df7c2`  
		Last Modified: Sat, 01 Feb 2020 17:55:39 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1475e2d19f52d98172917c76764e2976b8b028af977665dea09c24ca05d219b4`  
		Last Modified: Sat, 01 Feb 2020 17:55:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:28a1724975f0d3d915fdd4437bb6dff1248fcba149af3263baacda8d0df53103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ad1c476ad7bceefac0abce84dddcc784f382d48a39c1e7ace47011c45ffca72e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14827436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbd72c4a0ca324fa58904b89a1e3f7961c0c6f06d9fce279d56816a91dd9cc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:20 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 24 Jan 2020 06:18:24 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:24 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:24 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:25 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:25 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408f862d3a925084a8f20da4818facc02b5136b1c64af46aab594da9a00e6e2a`  
		Last Modified: Fri, 24 Jan 2020 06:19:15 GMT  
		Size: 11.7 MB (11736857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef248f2678020f581052347921213393abe2aef3bb16189ea7eb4feb23c7e819`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d0e4328be0f0ee7718f9879334e0abb572bb8941d9baa29140bccb00388dc7`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a0208ae33af327fb36eae423d4e90cabd9596b9d9b9f0b007ef0da70d8a78`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:28a1724975f0d3d915fdd4437bb6dff1248fcba149af3263baacda8d0df53103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ad1c476ad7bceefac0abce84dddcc784f382d48a39c1e7ace47011c45ffca72e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14827436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbd72c4a0ca324fa58904b89a1e3f7961c0c6f06d9fce279d56816a91dd9cc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:20 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 24 Jan 2020 06:18:24 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:24 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:24 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:24 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:25 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:25 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408f862d3a925084a8f20da4818facc02b5136b1c64af46aab594da9a00e6e2a`  
		Last Modified: Fri, 24 Jan 2020 06:19:15 GMT  
		Size: 11.7 MB (11736857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef248f2678020f581052347921213393abe2aef3bb16189ea7eb4feb23c7e819`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d0e4328be0f0ee7718f9879334e0abb572bb8941d9baa29140bccb00388dc7`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a0208ae33af327fb36eae423d4e90cabd9596b9d9b9f0b007ef0da70d8a78`  
		Last Modified: Fri, 24 Jan 2020 06:19:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:1cb60cb7eb92d77b620e6eadc5954cd15382d56dcbe675fe1a7a4c28151db5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:e6c379521b3ebf0bcfc7bda60d54478d30b1b6dcc4a411c90ce4ad9b770f3f8d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65396775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb07a18fe06e484e5a382233fe1ad22dbc87e57c320f58172e673ef68097f8d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:48:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 00:49:08 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sun, 02 Feb 2020 00:49:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 00:49:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 02 Feb 2020 00:49:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 02 Feb 2020 00:49:21 GMT
EXPOSE 8888
# Sun, 02 Feb 2020 00:49:21 GMT
VOLUME [/var/lib/chronograf]
# Sun, 02 Feb 2020 00:49:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 02 Feb 2020 00:49:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 00:49:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af64bbf8137f9e6bd074ef982a1129016ddcbe37866e214ea199a7f9f105be`  
		Last Modified: Sun, 02 Feb 2020 00:49:37 GMT  
		Size: 4.5 MB (4503576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf5631f93721d92c83bd1cbf1d06ef514652c88a29578e063d67e7873b0e793`  
		Last Modified: Sun, 02 Feb 2020 00:49:59 GMT  
		Size: 38.3 MB (38344098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51896fa76bc5a7aa40b0f0da3073a784be38815be9bc7f9c549fc5ce2599d19e`  
		Last Modified: Sun, 02 Feb 2020 00:49:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330ede3cc654c758b11df0588275ed9c6049df5272184587122b58e901666f0`  
		Last Modified: Sun, 02 Feb 2020 00:49:53 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210703d4a5d449f41a706a1614d73f9d6c316b1c30a1aad1e786386f0804f04`  
		Last Modified: Sun, 02 Feb 2020 00:49:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6329ff6d7821697751be5e271bca3eac84d112e2c66709ded61173ca70facede
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59013749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0ef024bcfcc1831d413bc1eb4a84ab245a174a1a3e67e9c5f17d0ec764807`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:43:14 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 01 Feb 2020 18:43:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:43:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:43:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:43:38 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:43:39 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:43:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:43:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611f132eaa9e78a937d09163db434cc699ec850c6a956b60e114e3d06645cf82`  
		Last Modified: Sat, 01 Feb 2020 18:44:32 GMT  
		Size: 35.8 MB (35800350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec15abccca3cd4183e9a6690bf71a96344a183d62977fabb35230d2c232645`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261c04826686c1e1dcbaaed0141369d992cca8524a67f58ddaab9ad9ac4bafd2`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e4d3bf6b962bdb74b686bdb3d745a1d8096f91d39bd46319d74ee428446d82`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2056ecca879b1a80688e00935b249d0c82b4f4d6b8fff6a9a66edd15e5af31c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60494364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2cd148be0d67747a943e380102c88ecb9185be7bb4dbcd1caa79fd66de7bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:54:21 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 01 Feb 2020 17:54:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:54:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:55:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:55:01 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:55:02 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:55:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:55:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ba1ebc98538ba96dd45ca27832a6d39a58f164cc7182edbc00154dbd946055`  
		Last Modified: Sat, 01 Feb 2020 17:56:03 GMT  
		Size: 36.0 MB (36003332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744e9d474940294854c8ea2446dce84039f5457247c5c97e5d67c56207513392`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba7e7c977114fc1347004bcc5ef6f4a3218dd40b400e91b850db2ef1523fb2b`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a86840da3d471928b27a8641246e91b07fc74a29be58318e76c5ff84535886a`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.16`

```console
$ docker pull chronograf@sha256:1cb60cb7eb92d77b620e6eadc5954cd15382d56dcbe675fe1a7a4c28151db5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.16` - linux; amd64

```console
$ docker pull chronograf@sha256:e6c379521b3ebf0bcfc7bda60d54478d30b1b6dcc4a411c90ce4ad9b770f3f8d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65396775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb07a18fe06e484e5a382233fe1ad22dbc87e57c320f58172e673ef68097f8d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:48:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 00:49:08 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sun, 02 Feb 2020 00:49:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 00:49:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 02 Feb 2020 00:49:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 02 Feb 2020 00:49:21 GMT
EXPOSE 8888
# Sun, 02 Feb 2020 00:49:21 GMT
VOLUME [/var/lib/chronograf]
# Sun, 02 Feb 2020 00:49:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 02 Feb 2020 00:49:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 00:49:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af64bbf8137f9e6bd074ef982a1129016ddcbe37866e214ea199a7f9f105be`  
		Last Modified: Sun, 02 Feb 2020 00:49:37 GMT  
		Size: 4.5 MB (4503576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf5631f93721d92c83bd1cbf1d06ef514652c88a29578e063d67e7873b0e793`  
		Last Modified: Sun, 02 Feb 2020 00:49:59 GMT  
		Size: 38.3 MB (38344098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51896fa76bc5a7aa40b0f0da3073a784be38815be9bc7f9c549fc5ce2599d19e`  
		Last Modified: Sun, 02 Feb 2020 00:49:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330ede3cc654c758b11df0588275ed9c6049df5272184587122b58e901666f0`  
		Last Modified: Sun, 02 Feb 2020 00:49:53 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210703d4a5d449f41a706a1614d73f9d6c316b1c30a1aad1e786386f0804f04`  
		Last Modified: Sun, 02 Feb 2020 00:49:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.16` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6329ff6d7821697751be5e271bca3eac84d112e2c66709ded61173ca70facede
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59013749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0ef024bcfcc1831d413bc1eb4a84ab245a174a1a3e67e9c5f17d0ec764807`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:43:14 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 01 Feb 2020 18:43:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:43:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:43:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:43:38 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:43:39 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:43:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:43:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611f132eaa9e78a937d09163db434cc699ec850c6a956b60e114e3d06645cf82`  
		Last Modified: Sat, 01 Feb 2020 18:44:32 GMT  
		Size: 35.8 MB (35800350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec15abccca3cd4183e9a6690bf71a96344a183d62977fabb35230d2c232645`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261c04826686c1e1dcbaaed0141369d992cca8524a67f58ddaab9ad9ac4bafd2`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e4d3bf6b962bdb74b686bdb3d745a1d8096f91d39bd46319d74ee428446d82`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.16` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2056ecca879b1a80688e00935b249d0c82b4f4d6b8fff6a9a66edd15e5af31c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60494364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2cd148be0d67747a943e380102c88ecb9185be7bb4dbcd1caa79fd66de7bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:54:21 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 01 Feb 2020 17:54:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:54:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:55:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:55:01 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:55:02 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:55:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:55:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ba1ebc98538ba96dd45ca27832a6d39a58f164cc7182edbc00154dbd946055`  
		Last Modified: Sat, 01 Feb 2020 17:56:03 GMT  
		Size: 36.0 MB (36003332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744e9d474940294854c8ea2446dce84039f5457247c5c97e5d67c56207513392`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba7e7c977114fc1347004bcc5ef6f4a3218dd40b400e91b850db2ef1523fb2b`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a86840da3d471928b27a8641246e91b07fc74a29be58318e76c5ff84535886a`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.16-alpine`

```console
$ docker pull chronograf@sha256:fb179947c124394dfe1ad86a69f8a5b3dbb71673c074a6274b9c3b0410291a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7.16-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f3b9c76d16e20144dace9f0a8a00d95a82c05e5209407d52be8ae1fe45993d8a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16d0f0f9db199994edeffe29a377125cf4c22db90b17980fb597280d987fcff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:32 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Fri, 24 Jan 2020 06:18:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:38 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:38 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:38 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:39 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe71ecdd62685580afe85276ea2d0243a8a2577f1324e8c512f797fef9dee135`  
		Last Modified: Fri, 24 Jan 2020 06:19:28 GMT  
		Size: 19.6 MB (19555966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df31809678f6d8cc5fcbecb90b4ed64398630fca3dd3427ea594fcf812f1c10`  
		Last Modified: Fri, 24 Jan 2020 06:19:21 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0071045c16456ab436c57d69aa6c07a03b8c1a52956957647fbe6feab766cd5b`  
		Last Modified: Fri, 24 Jan 2020 06:19:20 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b4b372df041bab39caf0f2afbc9fe8f703e3ccf9b5b826fab62077a7016d8e`  
		Last Modified: Fri, 24 Jan 2020 06:19:21 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:fb179947c124394dfe1ad86a69f8a5b3dbb71673c074a6274b9c3b0410291a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f3b9c76d16e20144dace9f0a8a00d95a82c05e5209407d52be8ae1fe45993d8a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16d0f0f9db199994edeffe29a377125cf4c22db90b17980fb597280d987fcff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:32 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Fri, 24 Jan 2020 06:18:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:38 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:38 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:38 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:39 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe71ecdd62685580afe85276ea2d0243a8a2577f1324e8c512f797fef9dee135`  
		Last Modified: Fri, 24 Jan 2020 06:19:28 GMT  
		Size: 19.6 MB (19555966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df31809678f6d8cc5fcbecb90b4ed64398630fca3dd3427ea594fcf812f1c10`  
		Last Modified: Fri, 24 Jan 2020 06:19:21 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0071045c16456ab436c57d69aa6c07a03b8c1a52956957647fbe6feab766cd5b`  
		Last Modified: Fri, 24 Jan 2020 06:19:20 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b4b372df041bab39caf0f2afbc9fe8f703e3ccf9b5b826fab62077a7016d8e`  
		Last Modified: Fri, 24 Jan 2020 06:19:21 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:fb179947c124394dfe1ad86a69f8a5b3dbb71673c074a6274b9c3b0410291a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f3b9c76d16e20144dace9f0a8a00d95a82c05e5209407d52be8ae1fe45993d8a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22646541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16d0f0f9db199994edeffe29a377125cf4c22db90b17980fb597280d987fcff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:17 GMT
ADD file:f4f85ec73d7cc949662413419f8eafb31dabaa6e12cd21b7c8d5a9ef0d5b9681 in / 
# Thu, 23 Jan 2020 16:53:17 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:03:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 23 Jan 2020 19:32:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 24 Jan 2020 06:18:32 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Fri, 24 Jan 2020 06:18:37 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 24 Jan 2020 06:18:38 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 24 Jan 2020 06:18:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 24 Jan 2020 06:18:38 GMT
EXPOSE 8888
# Fri, 24 Jan 2020 06:18:38 GMT
VOLUME [/var/lib/chronograf]
# Fri, 24 Jan 2020 06:18:39 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 24 Jan 2020 06:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Jan 2020 06:18:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9123ac7c32f74759e6283f04dbf571f18246abe5bb2c779efcb32cd50f3ff13c`  
		Last Modified: Thu, 23 Jan 2020 16:53:45 GMT  
		Size: 2.8 MB (2764173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018c3785b24046a24095a1f9cf7f42642c3dfd6e8282b328a2e22ce10ebc0de`  
		Last Modified: Thu, 23 Jan 2020 19:07:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cabf7ae254f2fa160de4e52dde588a8ed9490a15fc92b06cc1c47b680ccdf4`  
		Last Modified: Thu, 23 Jan 2020 19:33:23 GMT  
		Size: 301.9 KB (301878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe71ecdd62685580afe85276ea2d0243a8a2577f1324e8c512f797fef9dee135`  
		Last Modified: Fri, 24 Jan 2020 06:19:28 GMT  
		Size: 19.6 MB (19555966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df31809678f6d8cc5fcbecb90b4ed64398630fca3dd3427ea594fcf812f1c10`  
		Last Modified: Fri, 24 Jan 2020 06:19:21 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0071045c16456ab436c57d69aa6c07a03b8c1a52956957647fbe6feab766cd5b`  
		Last Modified: Fri, 24 Jan 2020 06:19:20 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b4b372df041bab39caf0f2afbc9fe8f703e3ccf9b5b826fab62077a7016d8e`  
		Last Modified: Fri, 24 Jan 2020 06:19:21 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:1cb60cb7eb92d77b620e6eadc5954cd15382d56dcbe675fe1a7a4c28151db5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:e6c379521b3ebf0bcfc7bda60d54478d30b1b6dcc4a411c90ce4ad9b770f3f8d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65396775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb07a18fe06e484e5a382233fe1ad22dbc87e57c320f58172e673ef68097f8d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:48:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sun, 02 Feb 2020 00:49:08 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sun, 02 Feb 2020 00:49:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sun, 02 Feb 2020 00:49:20 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sun, 02 Feb 2020 00:49:20 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sun, 02 Feb 2020 00:49:21 GMT
EXPOSE 8888
# Sun, 02 Feb 2020 00:49:21 GMT
VOLUME [/var/lib/chronograf]
# Sun, 02 Feb 2020 00:49:21 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sun, 02 Feb 2020 00:49:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sun, 02 Feb 2020 00:49:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af64bbf8137f9e6bd074ef982a1129016ddcbe37866e214ea199a7f9f105be`  
		Last Modified: Sun, 02 Feb 2020 00:49:37 GMT  
		Size: 4.5 MB (4503576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf5631f93721d92c83bd1cbf1d06ef514652c88a29578e063d67e7873b0e793`  
		Last Modified: Sun, 02 Feb 2020 00:49:59 GMT  
		Size: 38.3 MB (38344098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51896fa76bc5a7aa40b0f0da3073a784be38815be9bc7f9c549fc5ce2599d19e`  
		Last Modified: Sun, 02 Feb 2020 00:49:53 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330ede3cc654c758b11df0588275ed9c6049df5272184587122b58e901666f0`  
		Last Modified: Sun, 02 Feb 2020 00:49:53 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210703d4a5d449f41a706a1614d73f9d6c316b1c30a1aad1e786386f0804f04`  
		Last Modified: Sun, 02 Feb 2020 00:49:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6329ff6d7821697751be5e271bca3eac84d112e2c66709ded61173ca70facede
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59013749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da0ef024bcfcc1831d413bc1eb4a84ab245a174a1a3e67e9c5f17d0ec764807`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:29 GMT
ADD file:6ac430a42a1f2a6cc8b0a3565e518bd0e3a47b01d524b86cd3dd4e7f4606fd53 in / 
# Sat, 01 Feb 2020 17:04:31 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:41:53 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 18:43:14 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 01 Feb 2020 18:43:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 18:43:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 18:43:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 18:43:38 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 18:43:39 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 18:43:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 18:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 18:43:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6bc458b0813423b9e351a5604c0d71a4853d970ea22b23fedc8683af12dbc13c`  
		Last Modified: Sat, 01 Feb 2020 17:11:31 GMT  
		Size: 19.3 MB (19311624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f767a4ddc4b77052dac2b0b69478ffb671116744c71e02d18133e277dd7c19d`  
		Last Modified: Sat, 01 Feb 2020 18:43:54 GMT  
		Size: 3.9 MB (3877381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611f132eaa9e78a937d09163db434cc699ec850c6a956b60e114e3d06645cf82`  
		Last Modified: Sat, 01 Feb 2020 18:44:32 GMT  
		Size: 35.8 MB (35800350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aec15abccca3cd4183e9a6690bf71a96344a183d62977fabb35230d2c232645`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261c04826686c1e1dcbaaed0141369d992cca8524a67f58ddaab9ad9ac4bafd2`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e4d3bf6b962bdb74b686bdb3d745a1d8096f91d39bd46319d74ee428446d82`  
		Last Modified: Sat, 01 Feb 2020 18:44:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2056ecca879b1a80688e00935b249d0c82b4f4d6b8fff6a9a66edd15e5af31c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60494364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2cd148be0d67747a943e380102c88ecb9185be7bb4dbcd1caa79fd66de7bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:19 GMT
ADD file:d3338eed8ee88c2a5856cc2eb73701e4de79a7e551602df07834a1ad4f671435 in / 
# Sat, 01 Feb 2020 16:43:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:53:12 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 01 Feb 2020 17:54:21 GMT
ENV CHRONOGRAF_VERSION=1.7.16
# Sat, 01 Feb 2020 17:54:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 01 Feb 2020 17:54:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Sat, 01 Feb 2020 17:55:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Sat, 01 Feb 2020 17:55:01 GMT
EXPOSE 8888
# Sat, 01 Feb 2020 17:55:02 GMT
VOLUME [/var/lib/chronograf]
# Sat, 01 Feb 2020 17:55:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Sat, 01 Feb 2020 17:55:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 01 Feb 2020 17:55:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5c630fa6465ea72ddec15fd68bdd45a6da6fa4b1981895bf7c2852eedf066194`  
		Last Modified: Sat, 01 Feb 2020 16:48:58 GMT  
		Size: 20.4 MB (20385851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb406db3a5bf4f487242b44b5eb117d90608bc16921e74ddf810f1e61cfc5a3c`  
		Last Modified: Sat, 01 Feb 2020 17:55:22 GMT  
		Size: 4.1 MB (4080784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ba1ebc98538ba96dd45ca27832a6d39a58f164cc7182edbc00154dbd946055`  
		Last Modified: Sat, 01 Feb 2020 17:56:03 GMT  
		Size: 36.0 MB (36003332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744e9d474940294854c8ea2446dce84039f5457247c5c97e5d67c56207513392`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba7e7c977114fc1347004bcc5ef6f4a3218dd40b400e91b850db2ef1523fb2b`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a86840da3d471928b27a8641246e91b07fc74a29be58318e76c5ff84535886a`  
		Last Modified: Sat, 01 Feb 2020 17:55:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
