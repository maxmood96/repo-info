## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:3faecb090b45ffb5a6d2eaef4370e9e90a30cc13e2f788adb46b76e26196fd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:4dac54c3302638765f306a60ddb11999057db85d8997092fc17121c61a8e750a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55084900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e9f3e6d743c6ad2957d0a9022196a9ad012406d941562339b4e9ac76b0e7d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:29 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Tue, 13 Aug 2024 00:20:30 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:20:34 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41b64b6dba7d43a26aa677652f9ce4600819554efc51b1820828a2459e0b949`  
		Last Modified: Tue, 13 Aug 2024 00:24:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:06d7b0c086cdfc26790f4c64be4e07a42dcf8455740c9612ecfa3b1aed85f37c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52589216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc95eaba36353c6e13049b65abbca3061d67c5df8f5ba4947dd0600a133199`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:37 GMT
ADD file:1ad1c69027cf70fd9e0302f05fa38c8e0ba5f379ea0946e3cf3ff594a009c1c2 in / 
# Tue, 13 Aug 2024 00:55:38 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:55:40 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cb69e1e26795dd48d68a798670cc01030e737d07157119437dfe132cdf786177`  
		Last Modified: Tue, 13 Aug 2024 00:58:47 GMT  
		Size: 52.6 MB (52588991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff7437263eecf627dbf96056e52e3a82838c07da6050b1b23bd012bbfe654c0`  
		Last Modified: Tue, 13 Aug 2024 00:58:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:626615ada1436cf58e5b3545d7f7bf4ef9c56424d735a0886beedc9b260bb7a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50242559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55ea1b5b12e3029b4c2b0bc93a4ad6e19d71e68723ad80184d15e0e4e4a50f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:45 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Tue, 13 Aug 2024 00:57:45 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:57:49 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0236cf03661fe5867170fa43388500e996909fd053c4ed7c3eec17ae243555f0`  
		Last Modified: Tue, 13 Aug 2024 01:01:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d653153ebdb97a1f9debde885aa5f18b2e248806450ca5830310b1e417aa9c09
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53730146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c437ae87b567e2a38274fbcf8dc42b10c835ea3cb617bbbfd8fed31df512492`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:58 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Tue, 13 Aug 2024 00:39:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:40:01 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d78b93a7cebd9390e2045daea777315bef83b5b65dacb9898f002a0a3b5f23`  
		Last Modified: Tue, 13 Aug 2024 00:43:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:7c66e47d6472b66702ca7e09219cec76414e1adc959a89757c22787edc53fcb7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56074331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01454b542b5f8e3ec0146cf068886318e090397f6702e959bbb81d0084123d1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:39:11 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff49463f787141585aaa4bdaa3278d8f29a18f746862800c63356d5cc64b4a75`  
		Last Modified: Tue, 13 Aug 2024 00:43:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:1626e14b3ae6c03be457d4246033d00b0cecbdd64e7ec9bfa5ec6084b12fa4df
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53310785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e07e08cf1a7784eecb8c80ced908f35d07ba2a91ed52fe2323e6376ffa50e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:12:07 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ad418500d54bc2f053f193ded1b8b15daf2c07230d37a1a406b057fcb5466`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5d5d053b9818cdbdda62fbb3641ac413e3c8dabcc03bd9845ccc78923f26ccae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58954879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10527ba5de6ec294e6b55d88477742ba53ddb9bec66ddbde328435aad5776a99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:22:22 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae97a5d5c626f31b4961888ea7e0a20ebcd92391f616afb3f4e260b23233982b`  
		Last Modified: Tue, 13 Aug 2024 00:26:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:ab51cd1b089e3ba29f7ceff08506f5ed319b59e4b0b5f960e7dfc7f09d974152
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53324314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4dbf0ee9b4950fb5cb7f2e5308f988294dcece1c29bf100f288aba95676061`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:43:02 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895a4578ecc4753de3b712e7cac2696db9572caa8694936472df28fd00793ce5`  
		Last Modified: Tue, 13 Aug 2024 00:47:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
