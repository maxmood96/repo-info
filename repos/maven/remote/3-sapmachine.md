## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:266313709e27b9c99c9d4d798e671956764e57a3fb22eaaa18370495ad89bcba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:4360d92476e30eb26114be5dd6a3bc8f8e114a42b490043b8a8e7d50f02c94eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285961646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f2aae027aa069b89b7a19d1de51087b44b34d8c0b1c89dc8550618ee8b5a98`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 17 Feb 2026 20:32:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:32:14 GMT
CMD ["jshell"]
# Thu, 12 Mar 2026 20:14:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Mar 2026 20:14:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:14:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:14:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:14:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:14:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:14:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:14:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:14:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:14:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:14:34 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:14:34 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:14:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:14:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:14:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dd241bd37e489d34f787cd165d1a11f24b0c28a00cfa30c44e70c91094c547`  
		Last Modified: Tue, 17 Feb 2026 20:32:38 GMT  
		Size: 221.5 MB (221452841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb5de4678dd5fb0dff4f87e7d12c28c61ea50177996222299e6720dcf2ce95`  
		Last Modified: Thu, 12 Mar 2026 20:14:48 GMT  
		Size: 25.5 MB (25468980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42fc5c08db026dd3b814a48bf0a7605720d1bdd9408e09eeda38710748085c8`  
		Last Modified: Thu, 12 Mar 2026 20:14:47 GMT  
		Size: 9.3 MB (9311178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24addddb3eee21282437063ef3a6fd4868615c722d83e3714d1edb0c6057372a`  
		Last Modified: Thu, 12 Mar 2026 20:14:47 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d54fa107d3fb95e61bb0a49d8f47fa81306b6669f3a34ac52bf3c183ab2e18`  
		Last Modified: Thu, 12 Mar 2026 20:14:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:818a91b227a5f27ca1bc9ebe9b1bc130241906c567ad413a6a08444d95b1aea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4330793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3f0cec0bf2f7a98cb0b2f0af40970a2f370667b6c4529670bb7cfd8ee1d54e`

```dockerfile
```

-	Layers:
	-	`sha256:7808aa6f47a8a0e3d6b9f087934e6616859e62547e0acc48110cda0ee1687519`  
		Last Modified: Thu, 12 Mar 2026 20:14:47 GMT  
		Size: 4.3 MB (4313048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fe6e424ef81d572746bc3e1cd1589fea71c8d012c8cfcc9f78c337d6517be00`  
		Last Modified: Thu, 12 Mar 2026 20:14:47 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5775ef2471b7872c1fbb013bede99eb65adc5934111ae01640643feee4666801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282976674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c5afdb0de98e8e7c126210aa109492cd08f52c5842828a70ed723664dae3fc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["jshell"]
# Thu, 12 Mar 2026 20:13:21 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Mar 2026 20:13:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:13:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:13:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:13:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:13:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:13:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:13:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:13:21 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:13:21 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:13:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:13:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:13:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63210ec8e29a90dd08e5d25f72bdeb405e7aa2e604119720f6cb0ee9275c1387`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 219.3 MB (219265992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985497a1b3f45ffb5d38c681d938b62d9f47209712ef7d0552e0f8b210bad034`  
		Last Modified: Thu, 12 Mar 2026 20:13:35 GMT  
		Size: 25.5 MB (25533343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8775e8dce4bc85e07bd755d9980a48382867d7b0d40e5d9f9e12427f969a007`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 9.3 MB (9311181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8ad9d5ab8530908c6e4b10a7e4c2ce5a654361ec03e75ca58e2e4e696a0827`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c652beb2e046b50742b1cbdbc04c940775e2020f85715e95a15d95b65cc2b6a`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:319d7c08cbf77550e69cc74cac760ae245c4f9455452df24295fb17792f73f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1de6418e5c7d3ecc00ff7e0e64c197611e016e009c105745c1a5aaaacddd67`

```dockerfile
```

-	Layers:
	-	`sha256:e7d7e72d1d9990714ca263b2b3fad5f5b70dea532271db9e943aa799debfebcf`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 4.3 MB (4319615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e98e0c1c6c71fbb8ead62cff0cee66dcfd9277102c3658552a640bd3108309a2`  
		Last Modified: Thu, 12 Mar 2026 20:13:34 GMT  
		Size: 17.9 KB (17926 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:556522a284f3eae1ea89aeb3c9c9afd2edfdc6eaa4c4a848c9299a86e0ed35cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295994739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a20faf0b562ea16194295a6b065e1b0874df0f853844c577c4238620efbf0c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

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
# Tue, 17 Feb 2026 21:15:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:15:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:15:12 GMT
CMD ["jshell"]
# Mon, 09 Mar 2026 21:23:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Mar 2026 20:14:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:14:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:14:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:14:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:14:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:14:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:14:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:14:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:14:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:14:07 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:14:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:14:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:14:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:14:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ffd89d86dbd458a58533c359a539d854ce70cdc772c7d9f919cfaf14f31435`  
		Last Modified: Tue, 17 Feb 2026 21:16:03 GMT  
		Size: 222.4 MB (222382623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647fa706daa13b9fe27d687cc953cdeb6559d5a414dab24a86bfd1513d36c625`  
		Last Modified: Mon, 09 Mar 2026 21:24:04 GMT  
		Size: 30.0 MB (29992997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df78873050cbcac4cd486359a57fcae1f4d7eed44368d990c66944b87d35ae`  
		Last Modified: Thu, 12 Mar 2026 20:14:37 GMT  
		Size: 9.3 MB (9311175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3662c8730ece2fdf6550977e650d2b45c38ba3beeb57f9ac4cbc70ca2d871aa`  
		Last Modified: Thu, 12 Mar 2026 20:14:37 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3871bce7c14be1d28a52fdcdc0340a706c6d1d0f74ba8d9708435ea3837785a`  
		Last Modified: Thu, 12 Mar 2026 20:14:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:fb996f5632a139fafe62ed01926d8d0059a4c535d126287775095967422fa365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4330701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2079441fda6389f9a95fcce9bbc6c0bed70cb7fa108b06ca1db8d038cf4887`

```dockerfile
```

-	Layers:
	-	`sha256:1b0bd28c90f8cf27feb4ccc5aab4f1c3710e9bcefff43f98ca8ba748fcc851f3`  
		Last Modified: Thu, 12 Mar 2026 20:14:38 GMT  
		Size: 4.3 MB (4312883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bedbd037470c92252e5fca524e0be1805f653a2c024bbaf723c3efb896e77a16`  
		Last Modified: Thu, 12 Mar 2026 20:14:38 GMT  
		Size: 17.8 KB (17818 bytes)  
		MIME: application/vnd.in-toto+json
