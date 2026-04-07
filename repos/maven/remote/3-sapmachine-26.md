## `maven:3-sapmachine-26`

```console
$ docker pull maven@sha256:cf74960e6b7f1e5c8256326f9d4b15347b8a3c0cda5609332cb642fb3d012ceb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-26` - linux; amd64

```console
$ docker pull maven@sha256:1cc274b403925ddcff4b1a8edcecf021b9b785f17aae1b7e02995a48b2d4d778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290873914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7dfdb738eeb05a9e21293fca9c075ad35e318e513b2cfff27feb60417dd9012`
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
# Tue, 07 Apr 2026 02:32:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:32:21 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:10:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:10:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:10:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:10:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:10:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:10:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:10:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:10:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:10:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:10:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:10:38 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:10:38 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:10:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:10:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:10:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8266a02e110cb2134e191660ee2e9e59bcc2ef71d0f5533b48dfa541ddd65bc3`  
		Last Modified: Tue, 07 Apr 2026 02:32:45 GMT  
		Size: 226.4 MB (226358547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28968800bdfdd4dcd21704c998fc94b9cc6377dd2f77ce2b92dcee8385b269e4`  
		Last Modified: Tue, 07 Apr 2026 05:10:52 GMT  
		Size: 25.5 MB (25469680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69080a9d9cb824b6bf0ba597289a3b4d36908cbbecfbb1da35067df2e9022f9`  
		Last Modified: Tue, 07 Apr 2026 05:10:52 GMT  
		Size: 9.3 MB (9311190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b6f5b2d56b5e7cfe439bf7c83c00fc701dd29985a64685c83d42ba82153c1a`  
		Last Modified: Tue, 07 Apr 2026 05:10:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f795db002646392256a2c55fb4d9a98cca28839a931c12692b9dfb470558fa35`  
		Last Modified: Tue, 07 Apr 2026 05:10:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:33c8a30aff20b6aae2ea9b9f4e0e0a00dbddf27958c8fe9dd90ddf21bec613f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27841e410cb92833fe7ae0844803575eaa6743100de2d639531be876f3a04a0c`

```dockerfile
```

-	Layers:
	-	`sha256:2cee0aa58907542466aa9d69fa6b1250d924f1ce148766e88293d8f3bb9ab867`  
		Last Modified: Tue, 07 Apr 2026 05:10:51 GMT  
		Size: 4.3 MB (4311173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99de6d2658876b2757b15e1846a2ab40fcb46e3056e81e77bbf6f411a99af703`  
		Last Modified: Tue, 07 Apr 2026 05:10:51 GMT  
		Size: 17.7 KB (17743 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-26` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9eeeb6e24b3d450b603c659fe258d5c8b51aeb9d805f70716a2564bcc74fc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (287955019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8499213955b7cd17f7a7055973d5b2fdd4f802c55dd47c967e5ea518c46e4dbf`
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
# Tue, 07 Apr 2026 02:38:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:38:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:38:06 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:17:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:18:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:18:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:18:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:18:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:18:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:18:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:18:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:18:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:18:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:18:00 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:18:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:18:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:18:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:18:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e78fc1c0a6396b3a21b7cd7281de876a01ac981621033e1d5f2dc4b81420e3f`  
		Last Modified: Tue, 07 Apr 2026 02:38:30 GMT  
		Size: 224.2 MB (224235360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da1c84750cea6dd94386833037f0cf84cd72808d3fe4952f5df8d93f624b72b`  
		Last Modified: Tue, 07 Apr 2026 05:18:14 GMT  
		Size: 25.5 MB (25533364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d8084783c61a25883e098e95b9630c4513404cc2c213cc6e3c355bb46f7aaa`  
		Last Modified: Tue, 07 Apr 2026 05:18:14 GMT  
		Size: 9.3 MB (9311184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ceb463264c44d3d42ba35a2aa0367a46b2c4cdb400342a74bdbeb7f9a57a0a`  
		Last Modified: Tue, 07 Apr 2026 05:18:13 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3893d049b77220cc3052124d3626cf71de55fb73fa2ec84a2a7e1a4c8333b81e`  
		Last Modified: Tue, 07 Apr 2026 05:18:13 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:df7a949bc1193201288dcaf7f19df475b6286ff72a2a8d0204bd227066fbc282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c2dc0549009bb94ac970d68d2beda99a4d809e2d35d6036792f9357277ef3c`

```dockerfile
```

-	Layers:
	-	`sha256:9bb9e26e45e0874082b9d46da3697a15539c0932826f8fc78a1c232bd53e2c0d`  
		Last Modified: Tue, 07 Apr 2026 05:18:13 GMT  
		Size: 4.3 MB (4317740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc1e5da1595ea8c8f9abb4b86f2cb86094399c0b018ff08fbdefa157b727728`  
		Last Modified: Tue, 07 Apr 2026 05:18:13 GMT  
		Size: 17.9 KB (17926 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-26` - linux; ppc64le

```console
$ docker pull maven@sha256:b4ef387b66505c847889ebfc3341b1413a23644182dd83fbfc95320d85b2ed68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301237580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa218c8a50994bb9b9c8414ee88ced63b5fd1b1b39122976574fe5327096ee64`
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
# Tue, 07 Apr 2026 08:59:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:59:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 08:59:00 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 19:12:03 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 19:12:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 19:12:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 19:12:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 19:12:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 19:12:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 19:12:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 19:12:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 19:12:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 19:12:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 19:12:06 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 19:12:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 19:12:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 19:12:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 19:12:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aa874c6c717d7685ce22c8aecaac19624a6dc23b2cd3d9efb9fa9bf5766190`  
		Last Modified: Tue, 07 Apr 2026 08:59:43 GMT  
		Size: 227.6 MB (227616442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f8acbf9c58049c83385c00c1b448a696fe2ea71ac2a1cda8ebe1619dc81b9e`  
		Last Modified: Tue, 07 Apr 2026 19:12:39 GMT  
		Size: 30.0 MB (29995593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c1985af7d20be006a52e233b87550fc538c214acc2ce04e74b616811a985e6`  
		Last Modified: Tue, 07 Apr 2026 19:12:37 GMT  
		Size: 9.3 MB (9311173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1417f09719616df6a9cd1bc4766da9ea50cd8f657cdfecca8fb52df05f74e8`  
		Last Modified: Tue, 07 Apr 2026 19:12:36 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd9fbe26f0b59da5b44156292042d8c633de041d1788a974b563a0c856afef1`  
		Last Modified: Tue, 07 Apr 2026 19:12:36 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-26` - unknown; unknown

```console
$ docker pull maven@sha256:91ca80a81301d36565d613a6031448699802e4fb9097a0447238f760b4f58c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a55cd33555c77e68ac0e3b9025845ac0262952278d8d7faf153e9a6f7c6893`

```dockerfile
```

-	Layers:
	-	`sha256:b1edbb39c0c16097db14ba734fc7699bf63a7ded6b8e62d5be4e8449268de1d1`  
		Last Modified: Tue, 07 Apr 2026 19:12:37 GMT  
		Size: 4.3 MB (4311008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c97f43f1e03d45ea2b4a18f30a837b5186ff13dd2c0819454bfd79560393b26`  
		Last Modified: Tue, 07 Apr 2026 19:12:36 GMT  
		Size: 17.8 KB (17819 bytes)  
		MIME: application/vnd.in-toto+json
