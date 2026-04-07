## `maven:3-sapmachine-25`

```console
$ docker pull maven@sha256:a8a459db540ecd08cc9b4253d6471deb52eb1e5712cae57052e5b2814bdb6060
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-25` - linux; amd64

```console
$ docker pull maven@sha256:e0dfd722a54b2ed51d484beb127be2b2b91051b6e7be5dff1169d172fdc28a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285969225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52157d8668d7bb1ae014b188d249c91a3e3e6bc787d9323dc33f3c3eba96eae`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 07 Apr 2026 02:32:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 02:32:41 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:10:37 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:10:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:10:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:10:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:10:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:10:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:10:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:10:37 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:10:37 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:10:37 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:10:37 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:10:37 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:10:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:10:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:10:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b10bfa4727ab845dfc17be8eff800ac074681c0592ebf25fee26916dc79fa`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 221.5 MB (221453162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a64ee95a897d8abec92550aab21070c6deb5ef4b9517122e2f37d40faf8e91`  
		Last Modified: Tue, 07 Apr 2026 05:10:51 GMT  
		Size: 25.5 MB (25470371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efd4760121c7c722af6106f2643ef34c87a9bd1f0d6f9df7ae815127db28639`  
		Last Modified: Tue, 07 Apr 2026 05:10:51 GMT  
		Size: 9.3 MB (9311196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e8dd3847c74df1578a086f9517f7cb2a33057bbe4631bc07ff68df0b3bf3e8`  
		Last Modified: Tue, 07 Apr 2026 05:10:50 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb284ff4914cba7fd9b7ea965d8709321a15dad81efc9cb7f4bf62c04bbf73d7`  
		Last Modified: Tue, 07 Apr 2026 05:10:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:3e8cf10ee0321bc94b209884d82c0a87b4cdb08cca513bd6a3615b05e1e4356d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb663c53a5d3fb185e0f699d9c8ca68486ac825b1553d35decc49d8f297a781c`

```dockerfile
```

-	Layers:
	-	`sha256:31d32001f7aca5997ea9e51d5cef4ec45690799fabd310097e8525d37462604f`  
		Last Modified: Tue, 07 Apr 2026 05:10:51 GMT  
		Size: 4.3 MB (4311846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36cb55a2a499293a31bb5b09415e6ffbca5a9f8da31a0a2b0c2f01b8135698ec`  
		Last Modified: Tue, 07 Apr 2026 05:10:50 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:993f6edf088e2425036a935992d4c2a5956f4721665a39559154130b94f5cd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282986289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71b6535e5747ee7b232b8678156c334b553f7f7651067ab95dbe1dfdca8f091`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 07 Apr 2026 02:38:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:38:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 02:38:50 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:17:36 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:17:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:17:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:17:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:17:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:17:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:17:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:17:36 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:17:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:17:36 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:17:36 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:17:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:17:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:17:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071039733a9216930b6563942a42f349dfb95ab664b4c80b6dc59d7fdf8bb476`  
		Last Modified: Tue, 07 Apr 2026 02:39:14 GMT  
		Size: 219.3 MB (219266581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63771bffbfc5aab780b6bb041bc4ef2f83a5b674203d0857a66a376c163f7046`  
		Last Modified: Tue, 07 Apr 2026 05:17:50 GMT  
		Size: 25.5 MB (25533425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb3a7abc264da4ca539e1f28285b9ed6ddbdbc3cb2ad078a77239fe0a891cc`  
		Last Modified: Tue, 07 Apr 2026 05:17:49 GMT  
		Size: 9.3 MB (9311174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d28bb8cc1853b771f1688a15a65472e978345d2e82123c571416e294dca6b`  
		Last Modified: Tue, 07 Apr 2026 05:17:49 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0dc3e6da8e9af72f87c13e24b1f21737b38391ae5659a7ab910c32fb76ebe7`  
		Last Modified: Tue, 07 Apr 2026 05:17:49 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:3355179226dedacbdb1b5ea505001eeeb3d161d8cfe885b00a54326f58d81160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2002466c95cb4e2533c58def8ace988ee3cbc4afa0b90b9e8036212e7ff072f3`

```dockerfile
```

-	Layers:
	-	`sha256:e9a6b34a04f6bb56397bd2cc41280b553a2b6d5b829ca8fcdbf6e008c7b82427`  
		Last Modified: Tue, 07 Apr 2026 05:17:49 GMT  
		Size: 4.3 MB (4318365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7caff527d3fd6a3b42e5395b1c7da44d73a3f6eadeedebe0c1aee4ea0ff7c5`  
		Last Modified: Tue, 07 Apr 2026 05:17:49 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; ppc64le

```console
$ docker pull maven@sha256:8107e3c5b4b9781df4740e9fefcc33b2209ca20146313f04c3c4f96a0c349123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295972956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686eb1bd0cacf3bb985f246a2230a07d05a3ca0bab92ef91aa51da9c4cc675dd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 07 Apr 2026 09:02:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:02:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 09:02:49 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 19:10:41 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 19:10:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 19:10:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 19:10:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 19:10:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 19:10:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 19:10:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 19:10:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 19:10:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 19:10:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 19:10:45 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 19:10:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 19:10:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 19:10:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 19:10:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af1eb519a9c0294d2c0ffba67fd5006cf829710f4a208f1d662a7e0118dfaf9`  
		Last Modified: Tue, 07 Apr 2026 09:03:35 GMT  
		Size: 222.4 MB (222351673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af46e9999dc114229ca81489692e26995e8711a61fde58fbb8b4d4c0c51229b`  
		Last Modified: Tue, 07 Apr 2026 19:11:19 GMT  
		Size: 30.0 MB (29995737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fd7c7b6a5dc70a5d59ce1f46f43f0a6be90a1aedfac96587a8033832b7920c`  
		Last Modified: Tue, 07 Apr 2026 19:11:18 GMT  
		Size: 9.3 MB (9311173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496af7a5d453ec6231d124a1d8e444d7b7aa7e5e9344a03f35f59f2be953989`  
		Last Modified: Tue, 07 Apr 2026 19:11:18 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9658f4de66ecb60df974efc27da2dd34b0e27e07a178010059907cfe5c7516`  
		Last Modified: Tue, 07 Apr 2026 19:11:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:7ce255c6ef31dac5462c528273a209a66207b6b006f3efd1696fe77a797e53a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bdc945995ce43997dc0811ba56575505f29aa786a4423e44fa88edf5a778e5`

```dockerfile
```

-	Layers:
	-	`sha256:a037393806a22e90586cd24428568c465324774a39da2e4a2ca2b0044cdfb284`  
		Last Modified: Tue, 07 Apr 2026 19:11:18 GMT  
		Size: 4.3 MB (4311657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1866470a37143639090f55749bb976e1596ffe6529c0c621df44145f4d6f21`  
		Last Modified: Tue, 07 Apr 2026 19:11:18 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json
