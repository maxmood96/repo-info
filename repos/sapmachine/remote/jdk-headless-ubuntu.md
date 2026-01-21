## `sapmachine:jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:b474b2c7da1599af18bad1ca78b1e64addf9c176191d4687518b37356da2464e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:0a7d23031dc74b6922f7ac27831834d13f50941f81ac7ae6784c11d36eb08995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248963171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0338ce72cd7b9050fe06ea5323ad8789725f9b2253bf77628e334fc703d67f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:41:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cd072a4f288663499d336e5093f28279f389ee454abaa88131b8282fce988d`  
		Last Modified: Thu, 15 Jan 2026 22:41:59 GMT  
		Size: 219.2 MB (219237160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a6df9526c64d0f67d38cdd045bfc0de1f8c5b9db90211a40b793047d35999112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05e8b423a1bfb698499c9fe1742bcfedebb3f0c89165dac0cb6cfa34f804d0`

```dockerfile
```

-	Layers:
	-	`sha256:835fdd67402a2b7c0b00bec248db9c185e52990e8f60d840aaa487059fdc1a11`  
		Last Modified: Thu, 15 Jan 2026 22:41:32 GMT  
		Size: 2.3 MB (2348197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:252b42e8d99b64546888d914dcaddeef1c1b67b2796ef31641a1afee08a61564`  
		Last Modified: Fri, 16 Jan 2026 01:14:42 GMT  
		Size: 12.6 KB (12603 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7e8cd41e675966e4f24dabe012c0bfffbc1057534f443ff37ff475bd15a789ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245849646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d482afb81dc1a1b3c3e32b2b0b42dd1c84ef079253d0a64a8cb8bdae8d168d5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:44:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:44:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a22d05e6522ed1f6d389e368caf93e6ec73daf570ce9c3bd7edd30a5b1f6b1`  
		Last Modified: Thu, 15 Jan 2026 22:45:03 GMT  
		Size: 217.0 MB (216985822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c3ebbb9c9abacb5bf7f797c3ab0403acb688c336cde496a6354d79aadad8e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2361624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756408778a4828c776d775663a3a9dc7507ec395e249be7aa56f5c9c1b30f312`

```dockerfile
```

-	Layers:
	-	`sha256:a8c94eae1533e382d3c7e1076e7526e2f087871e9220c61d993fd2980d05f5c2`  
		Last Modified: Thu, 15 Jan 2026 22:44:19 GMT  
		Size: 2.3 MB (2348785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a8844429de7b0b90afcbce6690c261c00689b9ad8867c9997f2c3ff8ff8edc`  
		Last Modified: Fri, 16 Jan 2026 01:14:47 GMT  
		Size: 12.8 KB (12839 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:140375509902a94b56c091a967952eaefad937cf45e9ca9478bc8fe009c2ab05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254184866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1390a488483da6ab9bd0b38ec011c1df623e00c37aff915a84357cad8fccb35e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:25:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:25:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 23:25:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 07:12:18 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0daa586a49e23c5d661365aed5bb07edbd1bb2f2dfb32e94b17e0a7e56f29163`  
		Last Modified: Thu, 15 Jan 2026 23:26:45 GMT  
		Size: 219.9 MB (219878707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cee868867709d28983fecb6b054804e197bd4fc97e906ebc8cb30d78d67ff430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2356388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbb849e549b1d7f465233fb529718097184d6554a1082a2d5292f6004d34f8c`

```dockerfile
```

-	Layers:
	-	`sha256:d975aa27bc7de3f6e2852684eb235d08ff71a6594a92a382560760eb47c2be89`  
		Last Modified: Fri, 16 Jan 2026 01:14:51 GMT  
		Size: 2.3 MB (2343675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50508bb6f5e5873c0c0e669e7ed0a172e84ec0a9bdd89e6d9d1747308b9029c1`  
		Last Modified: Fri, 16 Jan 2026 01:14:52 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json
