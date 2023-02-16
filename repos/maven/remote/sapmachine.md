## `maven:sapmachine`

```console
$ docker pull maven@sha256:4509b8e42b9e0b52e41904d92a609b3bdb287d3ad7bb835e1d8cc2adee4be308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:9aefb8e881779a3aa9f536faeecc6e8e9dd35bed00e39b5448a8dedaf925e709
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273473122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f1ead02253502dad6ef6db4b119c211e233a91e857d4b12c8fb069a17f734e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:36:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:50 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:37:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:37:51 GMT
CMD ["jshell"]
# Thu, 16 Feb 2023 00:31:22 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Feb 2023 00:31:22 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Feb 2023 00:31:22 GMT
ARG SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd
# Thu, 16 Feb 2023 00:31:22 GMT
ARG BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries
# Thu, 16 Feb 2023 00:31:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Feb 2023 00:31:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Feb 2023 00:31:37 GMT
# ARGS: BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries MAVEN_VERSION=3.9.0 SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd USER_HOME_DIR=/root
RUN set -x   && apt-get update   && apt-get install -y ca-certificates curl git gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  apache-maven-${MAVEN_VERSION}-bin.tar.gz" | sha512sum -c -   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys   6A814B1F869C2BBEAB7CB7271A2A1C94BDE89688   29BEA2A645F2D6CED7FB12E02B172E3E156466E8   && gpg --batch --verify apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz   && mkdir -p ${MAVEN_HOME} ${MAVEN_HOME}/ref   && tar -xzf apache-maven-${MAVEN_VERSION}-bin.tar.gz -C ${MAVEN_HOME} --strip-components=1   && (rm -rf "$GNUPGHOME" apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz || true)   && ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn   && apt-get remove --purge --autoremove -y gnupg dirmngr   && mvn --version
# Thu, 16 Feb 2023 00:31:38 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 16 Feb 2023 00:31:38 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 16 Feb 2023 00:31:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Feb 2023 00:31:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128a3c2a925827e317bb305a000ec5d34677f8bb9d5359e30d27a1acbb8e125`  
		Last Modified: Wed, 01 Feb 2023 19:38:41 GMT  
		Size: 7.9 MB (7913384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d55b004b5a63431a7feffb61b7520f20068c280979145331f1749cd9a53a402`  
		Last Modified: Wed, 01 Feb 2023 19:39:17 GMT  
		Size: 198.1 MB (198080715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8979f90a0bce5ce3e54a8b175258574abb09b29e26d6965b83a7e51c1edced6a`  
		Last Modified: Thu, 16 Feb 2023 00:38:37 GMT  
		Size: 38.9 MB (38899926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd60acc047c43e027ab1022092c7faa526993e5710a66680e75b03e9944317a`  
		Last Modified: Thu, 16 Feb 2023 00:38:31 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc9f0f40d5054793bb80cf17755e65e62749ce30d671ad981b5c9932e2d1004`  
		Last Modified: Thu, 16 Feb 2023 00:38:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b369cffec2e2332bb140ada9ee09f881dc006f1ca84a8b19c983f9b716950d13
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269999463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af82e9213aa9dccd39b78e03d3c8eee4cf96f19038f579164aad9d66aecf85b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:52 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:52 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:56 GMT
ADD file:72ca0af0100de6591b59c44bd8856655c8441eb0fcbf7c32e427f6be5108a4a4 in / 
# Wed, 01 Feb 2023 11:27:56 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:07 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:12:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:12:09 GMT
CMD ["jshell"]
# Thu, 16 Feb 2023 00:47:55 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Feb 2023 00:47:55 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Feb 2023 00:47:55 GMT
ARG SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd
# Thu, 16 Feb 2023 00:47:55 GMT
ARG BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries
# Thu, 16 Feb 2023 00:47:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Feb 2023 00:47:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Feb 2023 00:48:08 GMT
# ARGS: BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries MAVEN_VERSION=3.9.0 SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd USER_HOME_DIR=/root
RUN set -x   && apt-get update   && apt-get install -y ca-certificates curl git gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  apache-maven-${MAVEN_VERSION}-bin.tar.gz" | sha512sum -c -   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys   6A814B1F869C2BBEAB7CB7271A2A1C94BDE89688   29BEA2A645F2D6CED7FB12E02B172E3E156466E8   && gpg --batch --verify apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz   && mkdir -p ${MAVEN_HOME} ${MAVEN_HOME}/ref   && tar -xzf apache-maven-${MAVEN_VERSION}-bin.tar.gz -C ${MAVEN_HOME} --strip-components=1   && (rm -rf "$GNUPGHOME" apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz || true)   && ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn   && apt-get remove --purge --autoremove -y gnupg dirmngr   && mvn --version
# Thu, 16 Feb 2023 00:48:08 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 16 Feb 2023 00:48:08 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 16 Feb 2023 00:48:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Feb 2023 00:48:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:70cf24b162395e1500d40f2b012f253bfd5d15f029ef9d636620fa2365ae503c`  
		Last Modified: Sat, 28 Jan 2023 04:42:53 GMT  
		Size: 27.2 MB (27193737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503cf1f0e33623621425996774370201f089f1e43bac7549f90ec52d7eea610e`  
		Last Modified: Wed, 01 Feb 2023 19:13:02 GMT  
		Size: 7.8 MB (7755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afab7854d2a348f242d4dd8183106fd8f0b2db6b5cc40c19f8c49a84184fa481`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 196.1 MB (196108261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775002cfd4cc30f480c5497d00f183f11bb68728460fec2ba1aabcf0cd5ee941`  
		Last Modified: Thu, 16 Feb 2023 00:53:43 GMT  
		Size: 38.9 MB (38940780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39493b275037359a3a67461917430e615a6157987bf2cdc98e6d0a3c5b3bcdef`  
		Last Modified: Thu, 16 Feb 2023 00:53:39 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2668645145e4fbeb866616903a60734da1c7430e0e33199df87aefc889ae9e06`  
		Last Modified: Thu, 16 Feb 2023 00:53:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:1549ec2fce6ed69920ddbd02dfafde333fc7923242ff9b5de20f10dc94877de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286523957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4abff027e1e447709f975b133016751966b089f44506426bea413aab7ada4e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Feb 2023 11:27:30 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:27:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:27:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:27:31 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:27:34 GMT
ADD file:987b941a34ad98533c64e74a3d57b9c1b983ff16c8f36e21d29278a30a2403ee in / 
# Wed, 01 Feb 2023 11:27:34 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:08:10 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:10:57 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.6     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Feb 2023 19:11:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Feb 2023 19:11:01 GMT
CMD ["jshell"]
# Thu, 16 Feb 2023 00:34:38 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Feb 2023 00:34:39 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Feb 2023 00:34:40 GMT
ARG SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd
# Thu, 16 Feb 2023 00:34:40 GMT
ARG BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries
# Thu, 16 Feb 2023 00:34:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Feb 2023 00:34:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Feb 2023 00:35:11 GMT
# ARGS: BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries MAVEN_VERSION=3.9.0 SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd USER_HOME_DIR=/root
RUN set -x   && apt-get update   && apt-get install -y ca-certificates curl git gnupg dirmngr --no-install-recommends   && rm -rf /var/lib/apt/lists/*   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  apache-maven-${MAVEN_VERSION}-bin.tar.gz" | sha512sum -c -   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys   6A814B1F869C2BBEAB7CB7271A2A1C94BDE89688   29BEA2A645F2D6CED7FB12E02B172E3E156466E8   && gpg --batch --verify apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz   && mkdir -p ${MAVEN_HOME} ${MAVEN_HOME}/ref   && tar -xzf apache-maven-${MAVEN_VERSION}-bin.tar.gz -C ${MAVEN_HOME} --strip-components=1   && (rm -rf "$GNUPGHOME" apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz || true)   && ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn   && apt-get remove --purge --autoremove -y gnupg dirmngr   && mvn --version
# Thu, 16 Feb 2023 00:35:13 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 16 Feb 2023 00:35:14 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 16 Feb 2023 00:35:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Feb 2023 00:35:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0c2f997991bfe2ed920105bb595c3662038cc90a08c6db9888fffdfa8c673b16`  
		Last Modified: Tue, 31 Jan 2023 18:14:55 GMT  
		Size: 33.3 MB (33300341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7ca009845dc04fb46ad30cf88116397b3027071f7bc7ae5faf7544b7ec00b1`  
		Last Modified: Wed, 01 Feb 2023 19:13:34 GMT  
		Size: 9.3 MB (9313607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2fea3b8447c3560525677504b1451371cf2f58ab7ea8c2b67e10d314511589`  
		Last Modified: Wed, 01 Feb 2023 19:14:33 GMT  
		Size: 198.2 MB (198223890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de84db90dcc5f2f8eff7bf1e4063077f3957f11882accd3c49443be61f5a3348`  
		Last Modified: Thu, 16 Feb 2023 00:43:08 GMT  
		Size: 45.7 MB (45684902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fd21e5b7518dd2e66ac198a4cb90bdeb01c4c3cc2dc4c23bbccd975ae40b1d`  
		Last Modified: Thu, 16 Feb 2023 00:42:57 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad44087927c896a96460dbb6d3df5bed7c61dac9e56edb8c412062640a2de74`  
		Last Modified: Thu, 16 Feb 2023 00:42:57 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
