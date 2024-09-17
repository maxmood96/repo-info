## `sapmachine:11-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:67e2ce159c63f7a47c711d88f63c30c3b36b56b4017ae76cce533589c9726ac9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:60ba9827aab771b259d68818ac65f4c7be1a58c81f6552b7f1c211fa1e9da291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229042505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b610cbb8e0537a3bac555a470f34728c1ceaa535a5c1eb53fa7442d121d1bf6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9749309d97463dc5e8499cfca00833aeb455456956155c1bb8be461a5844b1`  
		Last Modified: Tue, 17 Sep 2024 01:01:13 GMT  
		Size: 199.5 MB (199506817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:627f19f8678d05b157af9ea0e54a8ebeeced5fb057c770a39c20da80106b3723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24da3bba654a4453af6e379e0e8482dcab29b39c54903e535e0621468edd7f`

```dockerfile
```

-	Layers:
	-	`sha256:be95175881062ee5c45c409fee6dd6dfd044d32b1de2b381f5a0e48c6b743b0e`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 2.2 MB (2245890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f760249c500ec673898b32522b31be87a2f0299bcbdb7e148a7484a45193950`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 8.7 KB (8679 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:54a483d4fdec7da5815cc35616c1ddb29d21c3b6659f01ad2ecdc7663c956952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225338863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9fd37d1e20666d586637e055a4dc58fbde50205ad9bde65ada96786b20504c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a41e1e616613e031faf15bdb0cd5c497f67fa2d449cd9e4ea7d58a2c4463a47`  
		Last Modified: Sat, 17 Aug 2024 04:46:46 GMT  
		Size: 198.0 MB (197980180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1e52d2e8d287ba0d0aaa18d34ed7c4f2f11bd1dd0d2ee89af3705168e13f8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4bf5f964a62691f5c61c9e662b406bc74cc1b9c99c7519773e0e8851befe9c`

```dockerfile
```

-	Layers:
	-	`sha256:6dccb02fba1493103c739d69b215322b912bba80af0c71c0ce0c990a6dd73341`  
		Last Modified: Sat, 17 Aug 2024 04:46:41 GMT  
		Size: 2.2 MB (2246188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf162bfe661b167ad23fce866243fc31592de3058e4ea77d7279d17db48c8d30`  
		Last Modified: Sat, 17 Aug 2024 04:46:41 GMT  
		Size: 9.0 KB (8980 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:560d0962c6fcb702f6f2b627cfc467286141d30bc2f2d8afa245990843b44726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220441824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f341fc9c8efd1e5d759f0b89a546951c76e7dfa5027aa6f9cb56f3b85faa5e9c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e99e354ad4476324d62da56823e1992af776790a911419c7c1458020308b49`  
		Last Modified: Tue, 17 Sep 2024 03:07:53 GMT  
		Size: 186.0 MB (185993582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d9246a68d2dfa9bc03ad6667926aa54a12b4840125ec6ae2ce5a482d60b15eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d17c0089d1a5fef9a972bb5e450b326e8830a9c7d2f12ca5dda30224cf95574`

```dockerfile
```

-	Layers:
	-	`sha256:010462e3bafe013e0f4ce6c5d93c09824538122f9ac34f5933f98314d6043693`  
		Last Modified: Tue, 17 Sep 2024 03:07:47 GMT  
		Size: 2.2 MB (2247225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b038b17635da8d8aa2e93816fe17b6802b7d8b97486cd24f002442e82206acd1`  
		Last Modified: Tue, 17 Sep 2024 03:07:47 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json
