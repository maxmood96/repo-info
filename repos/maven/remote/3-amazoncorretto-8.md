## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:f1357bb4058a2a8cc87df7c8b52f28df5c698a100d464f281f3d0dc0e8f8573d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:3784a720afb76417e77e3b4df2ae3002d0d2ab252b525773c3acb1d96e58e431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352051952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ad1091fa63bf44ac6716838f33ffbcedcae5ce4598138b054752db17a0accc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:58:02 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:58:02 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 18:58:02 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 21 Jan 2026 19:22:24 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 21 Jan 2026 19:22:32 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:22:32 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:22:32 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:22:32 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:22:32 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:22:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:22:32 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:22:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:22:33 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:22:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:22:33 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:22:33 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:22:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:22:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:22:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2cf296d047513764ffd5d8eb73bd7e7516a94e3a350ef1d2cde26a84ada185`  
		Last Modified: Wed, 21 Jan 2026 19:22:16 GMT  
		Size: 76.1 MB (76119596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f80139ad0fb6bd343a84a2a25fd6c7dbb9d0f33babf371f86a90e0822b26c74`  
		Last Modified: Wed, 21 Jan 2026 19:22:57 GMT  
		Size: 173.6 MB (173614449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd5746944c77aa68ae71aaea380bc056536fe0685aedc7e60fd1fc8112bfb6c`  
		Last Modified: Wed, 21 Jan 2026 21:31:30 GMT  
		Size: 30.1 MB (30064472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6f6cc76d9a83507a49895fcff183266d00b786a28fe1b3b7667ddeb82d684d`  
		Last Modified: Wed, 21 Jan 2026 19:22:53 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee7475a97c7f6f6e17a14d629eff9abaeb8610875a01c5a07361af4bd620ada`  
		Last Modified: Wed, 21 Jan 2026 21:25:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5147c21ce15d497e8affb0d41b7e67a788aeedc848c6a9217752a392c5ecac`  
		Last Modified: Wed, 21 Jan 2026 19:22:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:a4a5f9341497981b50d1c13de18f86a5626435a80afbe14d966617bbac265694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3298f46d7a63f645d297a10740e3a0a7c6e9e2e64e19001d8a3f06b98086f3f1`

```dockerfile
```

-	Layers:
	-	`sha256:15b11ce721b3477c8d8f293a923c0aca6286535cd7ee1c4f6ee32e4eccfa31b6`  
		Last Modified: Wed, 21 Jan 2026 21:29:13 GMT  
		Size: 6.8 MB (6773617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bfe533acde9e59ce2cc1e0f528b1c897cb94534055cf862b82faa8c4f369435`  
		Last Modified: Wed, 21 Jan 2026 19:22:53 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1656ac58a5700e44ec9182eb78993dfa57327f8d59322bb971cdea0896e4fc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314665013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc3a1b9e926638abfc1943f153118bef3d4ec67622259210d6bdedce7d86389`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:58:32 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:58:32 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 18:58:32 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 21 Jan 2026 19:22:26 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Wed, 21 Jan 2026 19:22:34 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:22:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:22:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:22:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:22:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:22:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:22:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:22:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:22:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:22:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:22:34 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:22:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:22:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:22:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:22:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef0c3a8367555fd665644b39150b785e2d0486976224b943fc47236f954e820`  
		Last Modified: Wed, 21 Jan 2026 18:58:47 GMT  
		Size: 59.9 MB (59938538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905a509fc80591a4595bf882b50328956b5bb4918733af4e8ba2760a0cf7826`  
		Last Modified: Wed, 21 Jan 2026 19:23:00 GMT  
		Size: 149.4 MB (149436434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f12972e73f5a5d9e896d8ba6fd30aaf3ad0fc6a358dffc7738a00adfae80af9`  
		Last Modified: Wed, 21 Jan 2026 19:22:58 GMT  
		Size: 31.2 MB (31206323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8389f01f136b511147dc7916f51f791d4262c812b7d006a56f32a7569138fa`  
		Last Modified: Wed, 21 Jan 2026 19:26:43 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9976210e8164b8e8d588254fd64fd02480ff01211b9c1ee0257726a38973cc56`  
		Last Modified: Wed, 21 Jan 2026 19:22:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2611c7ef29205be007a6697c7b9c52a4b39908ebb118abf133d95e71cfde7d`  
		Last Modified: Wed, 21 Jan 2026 19:22:57 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:1d0e14a521352458e220d9c0abc7b95fcf241eaf5ece34da2c03aecdac806e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890d4dc01d679d75a1778e247283a7db76e8859e92c299909e0a64b191d56de0`

```dockerfile
```

-	Layers:
	-	`sha256:889ce84412c0538b5d95045a5ac3588d462346fc91d7434b38cb79a9d292c602`  
		Last Modified: Wed, 21 Jan 2026 19:22:57 GMT  
		Size: 6.8 MB (6750814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436553d72d637d3eb738909846b00c1927a51c6b31ca74666e273a92ce018173`  
		Last Modified: Wed, 21 Jan 2026 19:22:56 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.in-toto+json
