## `chronograf:latest`

```console
$ docker pull chronograf@sha256:36337a26f42df73c273f15841e64b1b898f1223f1aa158c10bebf668785a9d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:6bbfbbd73180964dbe313647223e80ee0e165ae05015db86639ba20f0f78931d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70424385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d0154a00f46e5c1657d665aa2fc18c9c0242b2db7f64caa4e6658ed6b4ef60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:30 GMT
ADD file:da0c935ddc86ca9e44bdd5f61b46c7b43a115ee4bc356324265a7ad6323f61ae in / 
# Tue, 09 Feb 2021 02:23:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:46:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 02:47:17 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 02:47:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 02:47:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 02:47:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 02:47:28 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 02:47:28 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 02:47:28 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 02:47:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 02:47:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cae7303ade7f17f84fe86b2a44880e9725cf7d6dcd17f79485360712b6af6dcd`  
		Last Modified: Tue, 09 Feb 2021 02:29:36 GMT  
		Size: 22.5 MB (22528600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603c713cc31395a01337edc5ae784741dda2d7aefb303bb93f7577486b1d1bbe`  
		Last Modified: Tue, 09 Feb 2021 02:47:56 GMT  
		Size: 6.7 MB (6742606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63600abc06b0687e4b24afa150d2da557c51a85b33e91502d51071591e5e6d82`  
		Last Modified: Tue, 09 Feb 2021 02:48:34 GMT  
		Size: 41.1 MB (41128782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b434ef96cd8f4643d0c998ec73edb0b44c26d4e31cd5bca7c5f29b9400a0d`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8145a040da7204ae6decb8f85b3096c06ade1972f6b6d4ab0496b789a24ce2`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391ffb32b78cc26585c3ddd4ecc5590a8961c93e839ed73b88da29e4ad507ee7`  
		Last Modified: Tue, 09 Feb 2021 02:48:27 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4bd93b3e7a1947354ca40608ba8679b477b93627fd704564f8844ec6583ae0ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63839627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31720bcd6ff8befefc1ba22809f3f7384cadcf9aac801b8e42422eba6027788b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 03:05:17 GMT
ADD file:42ae9de4db7ca66ccb0a5bc0291a00b2b1ad3c62e6e2d6bad1f99c693e981676 in / 
# Tue, 09 Feb 2021 03:05:19 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 06:43:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 06:44:47 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 06:45:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 06:45:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 06:45:09 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 06:45:10 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 06:45:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 06:45:13 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 06:45:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 06:45:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ebe5f2b760402bf53dfee026659ac0188dc5418dfde6839893f442bbfe23e42f`  
		Last Modified: Tue, 09 Feb 2021 03:13:48 GMT  
		Size: 19.3 MB (19316094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2a61da9a3e077953d6f78e9f324764fa0ee1dca73300f2c2e9453fc6ea84b5`  
		Last Modified: Tue, 09 Feb 2021 06:45:34 GMT  
		Size: 5.8 MB (5764950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37a1d6ec067d7ad885ae39385325d7b4d962e44a9606ac244f28cf7e0ef1c20`  
		Last Modified: Tue, 09 Feb 2021 06:46:18 GMT  
		Size: 38.7 MB (38734189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94bf3287fbb0eceb91a3df640fac834a6269be6dd059d7d74a2eaa6c45520d9`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01f4f97106955daa8a8383b91693e231660a91e456c56c3c0eb30856c6d2d4a`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd788b08bcc284b72a7696f72bfbabb0b3c44967caa6daaa71b425e112cc3a1`  
		Last Modified: Tue, 09 Feb 2021 06:46:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7f130666c6361906f40355f639d52098ddfb14057bc887b3fb0624dc46f071cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2a6436ea35a9248cd7a1fab7947bda22ebd1b384802f92f4381c3a4ab5995b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:38 GMT
ADD file:ec0f3f5aad51202b992acbfa7ec19738608d022983bc1918d7d9eecdd35e4800 in / 
# Tue, 09 Feb 2021 02:43:40 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:28:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 09 Feb 2021 04:30:15 GMT
ENV CHRONOGRAF_VERSION=1.8.8
# Tue, 09 Feb 2021 04:30:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 09 Feb 2021 04:30:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 09 Feb 2021 04:30:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 09 Feb 2021 04:30:31 GMT
EXPOSE 8888
# Tue, 09 Feb 2021 04:30:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 09 Feb 2021 04:30:32 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 09 Feb 2021 04:30:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Feb 2021 04:30:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b373a42fa9174db1e441a19411c9622d41f6db219878945ed0cb256efa32c8a6`  
		Last Modified: Tue, 09 Feb 2021 02:50:08 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b4b210d138fd2393967f174396ed44ec8cbf98472a90f6928614b79905e1c7`  
		Last Modified: Tue, 09 Feb 2021 04:31:00 GMT  
		Size: 6.0 MB (6028114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97054239d5610218f0d05723d441a14db8468a06c13285a97f969709773d4178`  
		Last Modified: Tue, 09 Feb 2021 04:31:38 GMT  
		Size: 38.5 MB (38502341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f43bc65242ba82f02506f64d85701f9c77545eb0b27c358b4485d6904721ad`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adfc4f590d599d4ffcc7b0942e21ba4bf06a0e9406b85dd3984a80066badaa0`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa90b76c984b1fd857a54f0cf52b49a189c1e0989ba0d5daba83447beb7041e2`  
		Last Modified: Tue, 09 Feb 2021 04:31:29 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
