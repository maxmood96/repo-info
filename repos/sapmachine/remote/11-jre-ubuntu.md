## `sapmachine:11-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:d84aad8119d8caa67ea78d372c2e6ac8306cc1a3ac0eddddf4f5481aebf71766
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:fccc579c68fb8d3fd9fe41e62fd2fc55a20d4afcbdaac0ba47b23b8bf504cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82490097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0553267aeea78c83cf7099bfe34ef114474a86abf2bba6bff9ab85c8226ff63c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984955d4e68dba0b2f2936df84c7fd917ab47463bfbd2f98092707f21597c12b`  
		Last Modified: Tue, 17 Sep 2024 01:00:49 GMT  
		Size: 52.7 MB (52740269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:df3a86cd3a327221f2cc338add34ecfde0f54bde2252195789d0ab2f30e9d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120449ed896b9234330f42aacb3379751fb03ec37d7f7bcb8aae729d990b89d3`

```dockerfile
```

-	Layers:
	-	`sha256:81625567d815830a96ed63664cd97eae2f634e96bedaa08190d610c149585059`  
		Last Modified: Tue, 17 Sep 2024 01:00:46 GMT  
		Size: 2.4 MB (2374825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f36dd4577550c140330aa248fe9fdd63b886126d215d5ea55d7fe98a1500b95b`  
		Last Modified: Tue, 17 Sep 2024 01:00:45 GMT  
		Size: 9.2 KB (9216 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e79b4a39c88f03d4137655eebfcb281bd29396c12f98babfcc085d9ac9757f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80779453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85976212faf578ab7a5a0cccd0a43cdad55c9ed196f6c526df09d713e359f69d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14418bc7bf4b62cbf13351c7aa3e047dc9b6166d04dbe557cc7664746d84de70`  
		Last Modified: Tue, 17 Sep 2024 03:37:28 GMT  
		Size: 51.9 MB (51893854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f1b65f2c1a38e8e41ee3933074111760ffa0953733bd444eee3a13cf1007a9f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d04a34f4de4972edc6371266b17a344844959608573aff57a003022f6312d6f`

```dockerfile
```

-	Layers:
	-	`sha256:4f954d52b343a9f3bd79aee6a6d018c3601d77b95c42afbf170e5cea9ecd9611`  
		Last Modified: Tue, 17 Sep 2024 03:37:25 GMT  
		Size: 2.4 MB (2375944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4456cd53711c6cc0b1a0bd39b904858d0ff7ac7a85b880c74c1a8e916ee7cc24`  
		Last Modified: Tue, 17 Sep 2024 03:37:25 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1aa77859685652268440c59a609a5ec355099ca6e5006a8d76d9a1fcbf2af06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86106537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73e043e2a09a28fbecc29cb1e3d0d066dd0a1edb790d491526ca0fa18ff6b11`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd552476333d2f12762aa5cf4944a66426fa2f44d0180c7c65a89724d1c5d620`  
		Last Modified: Tue, 17 Sep 2024 03:01:45 GMT  
		Size: 51.7 MB (51714192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c14b585250ffa518c16cf7c1cd3f44e5b51a5ba8ba4148414ff175d8f583c561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ee1f621788559b8c8fa1259661ce7514403a79bcb17a9422a90f3b4a71d656`

```dockerfile
```

-	Layers:
	-	`sha256:198d345f75f3456e5e2bbe040ed0268c1c9a24e6e6602d60cdb0bd2c878b8d91`  
		Last Modified: Tue, 17 Sep 2024 03:01:44 GMT  
		Size: 2.4 MB (2378780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3f72a14f813da7ef572d0ec25f4e4aa938238277ebdfe520b1eb36227fe446`  
		Last Modified: Tue, 17 Sep 2024 03:01:43 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.in-toto+json
