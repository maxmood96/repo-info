## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:1ee42b53eee995ea7c1966b10c894900e1513b07548ab01fe52467ae63465eea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:314bae9b06d834a0dc656231d05157fd8a08ae880956d73fb97451ba517e5516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279790292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2c06d46c9a8b57022a2d974357e47e5d6073ee840474f5b5da75120a14cb04`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:25:17 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:25:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:25:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:25:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:25:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:25:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:25:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:25:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:25:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:25:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:25:17 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:25:17 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:25:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:25:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:25:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90deaade267143332d1a757f5a5baf9e834c273db1dc217170fea3446a6932b7`  
		Last Modified: Wed, 22 Oct 2025 03:37:35 GMT  
		Size: 215.4 MB (215361388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8c0b3deb3ab46a44775e4e48c87a1607a31a3095cc06b10b484e5cc8ff864d`  
		Last Modified: Sat, 08 Nov 2025 19:25:42 GMT  
		Size: 25.5 MB (25462118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22d13605ef5ca87e18f4163b8cfd10b0e2a8f9507905fc9df119518adc21e4f`  
		Last Modified: Sat, 08 Nov 2025 19:25:38 GMT  
		Size: 9.2 MB (9242606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ddcb3bf592a6fb3fbfc2fd56ee4e3309ee0c804a64f8adaf9f04158bb8bec5`  
		Last Modified: Sat, 08 Nov 2025 19:25:35 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ac49f35f46f7876fc8beaff8e994a7cccd2aaf720413077e1504c28b51cb9b`  
		Last Modified: Sat, 08 Nov 2025 19:25:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:800c371fc51bd88e896db65c1ad4f203149760d9aa86248fd97eb487cb8d8bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4336480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601415b1b77026e909bfcb408cc7396dea0c4e5a626b9011ca37b680b8b5b1e3`

```dockerfile
```

-	Layers:
	-	`sha256:46594c9b0f97bdf8ab3ed594554864aceb020f676e5c91b734e23e0b70563d4a`  
		Last Modified: Sat, 08 Nov 2025 21:33:38 GMT  
		Size: 4.3 MB (4319977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:575c3442e8c3c8daf05b375f9c6d14fa2e692d20c31e688821a4da893626f7d5`  
		Last Modified: Sat, 08 Nov 2025 21:33:39 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7c0c97b1f5c2c6408b2a4b9f77233f35b9c5bdb757d9c5cf5526fcf553c1637f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277255302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adb57e64151c0258eb3b83a9944c63285521c63419b45576c05e7f77b71befb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 19:24:47 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 19:24:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:24:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:24:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:24:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:24:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:24:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:24:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:24:47 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:24:47 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:24:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:24:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:24:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7071e302a1a5dff6b5e6e89543863d918141db2376a55576de31929df5e87150`  
		Last Modified: Wed, 22 Oct 2025 00:10:00 GMT  
		Size: 213.6 MB (213617780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb332eb0221964ba847c8a593ece5f6abba7fa0118efd9e5fc06365650f2e5aa`  
		Last Modified: Sat, 08 Nov 2025 19:25:13 GMT  
		Size: 25.5 MB (25532193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f650f7caf56c0cced38e6e9d82a41cbce6c25c5181e61e4e78492d4326df310`  
		Last Modified: Sat, 08 Nov 2025 19:25:12 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4441b57c1da123b5d4aa5d9897e30b8c62b32708613c48a0b6fa7d4234ff1bc1`  
		Last Modified: Sat, 08 Nov 2025 19:25:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7b6d094582a3e01c38dda40f4d2fb5bdf1eb2989298444dfd41c87651a6876`  
		Last Modified: Sat, 08 Nov 2025 19:25:13 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:45117f1db6a6f92bb31330e66661130fa4dae35e0999e3e68f35819710d2f2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08aad7a9fac5887fae68d25fafeeb295a8a32a6e2c449854c60aee7a226c84e0`

```dockerfile
```

-	Layers:
	-	`sha256:604c040015b30186b8f95b252430b01f354fcee28ab9e5c4eae539949a9a86d7`  
		Last Modified: Sat, 08 Nov 2025 21:33:43 GMT  
		Size: 4.3 MB (4326499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c3e550bf969b151f9d2a1b81304512ee1eeb35b460aa25f0d5bd3a20462e23`  
		Last Modified: Sat, 08 Nov 2025 21:33:44 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:6cf8287debad58a976fe6c96ff1fbbe71cb2f2d7453c64a57cdcd55dcaab5c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289846234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c95c8d641da7df8f9e9ec7c212e5a24d4433a1bdd8365823addcb7e997fbe96`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 22:43:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 22:43:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 22:43:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 22:43:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 22:43:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 22:43:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 22:43:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 22:43:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 22:43:10 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 22:43:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 22:43:11 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 22:43:11 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 22:43:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 22:43:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 22:43:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d86bfd3a18c669589bd408d0764b715ca6dbf05f6beaac8f7f8d6a4e59f39a9`  
		Last Modified: Wed, 22 Oct 2025 14:29:02 GMT  
		Size: 216.3 MB (216312643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6849e7abd4290caadf7f0778fbc7f5880c2fde18d6a900b5a58f067de9652`  
		Last Modified: Sat, 08 Nov 2025 22:43:54 GMT  
		Size: 30.0 MB (29986452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a57317165ee8459fbfd673693ae177aafa81540232a50afb87b34f86bb525c0`  
		Last Modified: Sat, 08 Nov 2025 22:43:52 GMT  
		Size: 9.2 MB (9242574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e85945f7acd909acef94e0422368493700be700c387c061a8dd3b59978a8da`  
		Last Modified: Sat, 08 Nov 2025 22:43:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef93fe7033c34f282654f8e37a3f1d6e31b405bc0a87d51cafffd3509c5e5eab`  
		Last Modified: Sat, 08 Nov 2025 22:43:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:1dc0482e15711a31a614eb20ed6c77d88d56a4276e83fd6c708a0051bc2c1bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4353c17e01c2563966cd046d079e8fed1d1ea3bb23024d4c20e41609ec9d92`

```dockerfile
```

-	Layers:
	-	`sha256:75f8aa4a046c0990814f1405874e6b92905a062ffa765a2aca3c7d11f0e38ac2`  
		Last Modified: Sun, 09 Nov 2025 00:29:33 GMT  
		Size: 4.3 MB (4318989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b871c553354d06334c7d469c3832c524d5d7e1748a809bf7174dec1856f3b2`  
		Last Modified: Sun, 09 Nov 2025 00:29:34 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
