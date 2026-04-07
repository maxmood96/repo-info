## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:962f427328e49a71510c8da63f6d55a4f39668da974ab8aea2e8af1c173b4e94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:c613d5c9d5e2fb61b16463955e004a22c6878595efdd68aa826f6af1f3b31eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230245588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639549edba87853f46f9d699b7483e8d8762578a1c80eee94bf71108e263a3ee`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:33:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 02:33:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787c7c0d05e6c06020997776f0752b607ad6162706cc11f5099eeaa6253f284b`  
		Last Modified: Tue, 07 Apr 2026 02:33:56 GMT  
		Size: 200.5 MB (200512129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b302ba2818ebff879f2cb424ca62d470f8e224656dc96ff36e192ce1f85e1219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a51eba85caa74e745e99b6649a82723184b5a1dbf5bb2965d4de98bebb775d`

```dockerfile
```

-	Layers:
	-	`sha256:96110e9708110c98e82f99df1741c403e83b8c1e9100e3772a5ee6a744dd837b`  
		Last Modified: Tue, 07 Apr 2026 02:33:47 GMT  
		Size: 2.4 MB (2356888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b562e45e4d7e03824dfcd096f334b4fe9366f900da06e94aafc3f53c6cb1fd8`  
		Last Modified: Tue, 07 Apr 2026 02:33:47 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a5bac535fae486df5c91509c13571187b758c40152448fff1750035c5aea5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 MB (228101706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320f25cbe872c7104e5f9b7af76ed71c7cfc4f96d5a5c1b63d15dbddc66b77fe`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:39:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 02:39:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5831340709a5b137e3fb01df449edda2edcf3b69e6ca6b89052ab6cb74f8e623`  
		Last Modified: Tue, 07 Apr 2026 02:40:01 GMT  
		Size: 199.2 MB (199227631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a5c2e399ae7bc20b51af6318d518004d5b8b1d7286b61e131cd871c90a1c18a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a457ef935628d7487248edc4e2befe151fb0437a81b64705ab0adb00167cb1f5`

```dockerfile
```

-	Layers:
	-	`sha256:165bc37789f2226a7d5ce7ffdfd01e942e0b36043845353a0003cd408357375a`  
		Last Modified: Tue, 07 Apr 2026 02:39:57 GMT  
		Size: 2.4 MB (2357395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dceeb68b77fa6f68a531bb8a9170348329885956099e372a78dd4f3e6a9c78f3`  
		Last Modified: Tue, 07 Apr 2026 02:39:57 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e629adb4a9214280c31e2c431f46ed96eb384dcf31561d356b7443476e389837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235490810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4f24d555a439e7a25dc630a61c4cc4da922d0e8e0417569236ec5402554d31`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:11:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:11:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 09:11:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5615cc34c37269d7066e166fcf834f966ab128cf40fc521c3ac50a24653377`  
		Last Modified: Tue, 07 Apr 2026 09:12:17 GMT  
		Size: 201.2 MB (201177476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:444b30306214623d1081d11b9bcdcc02b143bc23520a50baff57301bd914e8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708aea2ff6b40de2271d8dc000a411d4f21f2a48f414782fb3e7e4d19d2b409`

```dockerfile
```

-	Layers:
	-	`sha256:91b4b1fcad1368e74c0e1e837e98b41c766a76a06eefc15309e15ba07a6dd5e8`  
		Last Modified: Tue, 07 Apr 2026 09:12:13 GMT  
		Size: 2.4 MB (2354359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fa8c0927ac000338a29a42d801d9209143aab3c3698f111efe0acec070d0a0`  
		Last Modified: Tue, 07 Apr 2026 09:12:12 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
