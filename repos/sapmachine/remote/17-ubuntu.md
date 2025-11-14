## `sapmachine:17-ubuntu`

```console
$ docker pull sapmachine@sha256:a7c01d3ded2c049b0fc8e675bf7ac147c77d1be366cbb25e1eda1688d950dd76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:e03560106cd392e1e934423b3710ee80cd3ab93c6ffbcb21a73ef1a8a48a5715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230393764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e1a3c5c982a6bb7c55cecd7a629096aed762ecac8b92df23df2358ef69c834`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631b1914a3f666b03be170977fda73e9d2f60cdeff1977715823aa31a3ac6184`  
		Last Modified: Fri, 14 Nov 2025 01:08:08 GMT  
		Size: 200.7 MB (200669076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d0ce1c08cf8b22e4ac0630ac923304194059b971d3b5fd5372d622b4f99a64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9855795481eda01fb71dcdf26bc870989e94608fc87c881ed5063355ba98da8`

```dockerfile
```

-	Layers:
	-	`sha256:462b566806fb06bbd4eafb2b25fbd7cff0aa6f597521ab1e6751eb9b6610a960`  
		Last Modified: Fri, 14 Nov 2025 01:06:31 GMT  
		Size: 2.6 MB (2602850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c799ca2be3a92fd42700c1020ae58aa818b26da5b5f65e8f6067f9f84c70ab61`  
		Last Modified: Fri, 14 Nov 2025 01:06:32 GMT  
		Size: 12.6 KB (12606 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f178b4d1a2184366d11d20354c4e0a385c2567bbd20b90443fabd01754acf0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228254121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dbdc25816162c1ea045a743fc09d5bf72201cbe35eb91bc8998eca78b00010`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:38:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83709b1cbcef0ca40d50087b6293d8e8293235be7fe636e4c606ce2dbb43e6b`  
		Last Modified: Fri, 14 Nov 2025 01:59:45 GMT  
		Size: 199.4 MB (199392164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:df0947e278a3dcfab3491a82f03d386dd4f1dcf1474b322626c092e9e721aa2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b285d8bb663eefea2074209bdc2da868553f08e0e9e1ac77b67aac3ba492f2`

```dockerfile
```

-	Layers:
	-	`sha256:2266c831ba81eb4fc7449744dd9c0988e29641e94441034ef48043f3b2682882`  
		Last Modified: Fri, 14 Nov 2025 01:06:36 GMT  
		Size: 2.6 MB (2603462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0397ff35eb6151d30188797663e02153444fb49b0c852192a511d5383c9f1651`  
		Last Modified: Fri, 14 Nov 2025 01:06:37 GMT  
		Size: 12.9 KB (12855 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7d89c683dc1f023307b7c968142963abc11642c68f13d4cf32d1700e626ac6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235758688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4864d480042488c4606ec7cd67d8439c72146cb07cb7a19d3d3e703a47c03db3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7ecb53327d7a17c33f59ea456eb56d4ff5903b48e30e5849e3cdf6584eb28c`  
		Last Modified: Wed, 22 Oct 2025 14:28:57 GMT  
		Size: 201.5 MB (201455163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:305ac3aeda1404777a648fc3c2cb3137c5e4fe6506551850c6442e16595ac5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2046e8279a633cb40c30b60c6d39b16e645c2282e68942f9af5959c1a8c0e0ae`

```dockerfile
```

-	Layers:
	-	`sha256:c130b5de815595a2f2eb8940c47e4f7f7b90ec0028f2c84f1a71e4bbc45f1fe9`  
		Last Modified: Wed, 22 Oct 2025 15:04:40 GMT  
		Size: 2.6 MB (2599033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:782963b9211ebf2c99ba059ab613fd23ec21298d966c406d911549f7d2eecbad`  
		Last Modified: Wed, 22 Oct 2025 15:04:41 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json
