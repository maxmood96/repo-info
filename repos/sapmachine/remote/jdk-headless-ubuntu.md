## `sapmachine:jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:45d58d5c424cdba32615b60759392177ddaea99e5582c2df6c72944c9d1ac2b8
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
$ docker pull sapmachine@sha256:d283cf7cfae0e83d57d73af93f00be6fa8fe9713ef51f89d7344fc7be23cb146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (250010583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4926e8b748a2be595dbb2735ea38b271fef7041aedb7d68591059cc91c1a7b6a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:32:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:32:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c5096f1407791710252c7f28482315a404fd0c7ec9ab88112791af45bca59a`  
		Last Modified: Tue, 17 Feb 2026 20:32:55 GMT  
		Size: 220.3 MB (220282972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a341a6b9839918351af47e1b1979d343d726e0fccc3110b0f50a68f1f2410f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c197f441d3204f055163c024b996cecd130a9892f374c767f740387d143c89`

```dockerfile
```

-	Layers:
	-	`sha256:e0ded39ae2cc603f4e6c633011ed18ed9e83d7005eb81d414edc3adf9b898d9f`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 2.4 MB (2350561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306440dd1cd739212867f9b7014fd2e2745945e02185a2b721754369e08b0406`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 12.6 KB (12603 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3e0d621b139347bf43fe8361c39a12c1bc1c76c3fdbeb2ed59fb3b25bcc0f91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246933440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cd1d9af9ce6ecff1f54fa7e65831b71c8667ccf35d0f11d7f167e11a1e45d0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:31:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:31:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317979e2ce9f071739b746c48a0cb08b6cb3a1149e05df295c62a4772ff6e180`  
		Last Modified: Tue, 17 Feb 2026 20:31:50 GMT  
		Size: 218.1 MB (218068320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38b344dc8dfed1f0b6df7c9bf6a3c7d1fe31d0ab21e8f7f324591075d14c11c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435fb659636351c783f14dc709bc34ed853a2e3499286029e336bc39e6cfd6ac`

```dockerfile
```

-	Layers:
	-	`sha256:ae0f206fd16537c3fa102b6e7887244182950324c3b873bb24582916f6615979`  
		Last Modified: Tue, 17 Feb 2026 20:31:46 GMT  
		Size: 2.4 MB (2351149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4318070f847e5cb8ba807390f859e6b6bffe36a2d5c8a8ae14dff3016a378ead`  
		Last Modified: Tue, 17 Feb 2026 20:31:46 GMT  
		Size: 12.8 KB (12839 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:053e4e8a38c838fa91ca79bfbddd5943cff83287462511ec43e46b4c609de215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255306208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fa5b8a976cae562fc8dc05268e6722af1b20cd3f27e93bc7e3071edf06ebba`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:17:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:17:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:17:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c9fa42ed7f0bee9283e7b64b9a8d15ebc1cf2bc5eaad0d2dbb7f6c5af6b51`  
		Last Modified: Tue, 17 Feb 2026 21:18:06 GMT  
		Size: 221.0 MB (220999302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:faa00ffe3337cd22846dbc9ce1c51b86ec1d47492b3cb68a008d3e47d4c01446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c28ebec7e2e3caef91ab6d4c801dfa473ad99befa5c28320eed3cb62d02bc2b`

```dockerfile
```

-	Layers:
	-	`sha256:3308b8d8ce251c13fbd41c4d3b3280eb3630f2b8081809786a533b44997b297b`  
		Last Modified: Tue, 17 Feb 2026 21:17:59 GMT  
		Size: 2.3 MB (2347456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959ae814da5ee1d5223713cb3bd03bc4399e882c5fdb4e32bcc123acbb68c980`  
		Last Modified: Tue, 17 Feb 2026 21:17:58 GMT  
		Size: 12.7 KB (12712 bytes)  
		MIME: application/vnd.in-toto+json
