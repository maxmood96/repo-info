## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:6afbdcee7a6809b219b2fc5fc8db101aab29f1446a54bef62b8c21f120bf55a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:d62dc61a40013ec66f47b4724ccf5c742e4c832af18486509e2410e322fcdc7e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (227006688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923378d00a618859654a82e8f06cbc44ca32a87a25023f83532933de8c590276`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 22:20:04 GMT
ADD file:6ebab25a4f1aa82238dbf1a48f38d22c6421052d0d158cf88cbc1a4d01b5c5c1 in / 
# Thu, 26 Jan 2023 22:20:04 GMT
CMD ["/bin/bash"]
# Thu, 26 Jan 2023 23:10:07 GMT
ARG version=17.0.6.10-1
# Thu, 26 Jan 2023 23:10:31 GMT
# ARGS: version=17.0.6.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 26 Jan 2023 23:10:32 GMT
ENV LANG=C.UTF-8
# Thu, 26 Jan 2023 23:10:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 16 Feb 2023 00:29:33 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Feb 2023 00:29:33 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Feb 2023 00:29:33 GMT
ARG SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd
# Thu, 16 Feb 2023 00:29:34 GMT
ARG BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries
# Thu, 16 Feb 2023 00:29:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Feb 2023 00:29:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Feb 2023 00:29:49 GMT
# ARGS: BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries MAVEN_VERSION=3.9.0 SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd USER_HOME_DIR=/root
RUN set -x   && yum install -y tar which gzip   && yum clean all   && rm -rf /var/cache/yum/*   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  apache-maven-${MAVEN_VERSION}-bin.tar.gz" | sha512sum -c -   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys   6A814B1F869C2BBEAB7CB7271A2A1C94BDE89688   29BEA2A645F2D6CED7FB12E02B172E3E156466E8   && gpg --batch --verify apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz   && mkdir -p ${MAVEN_HOME} ${MAVEN_HOME}/ref   && tar -xzf apache-maven-${MAVEN_VERSION}-bin.tar.gz -C ${MAVEN_HOME} --strip-components=1   && (rm -rf "$GNUPGHOME" apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz || true)   && ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn   && mvn --version
# Thu, 16 Feb 2023 00:29:49 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 16 Feb 2023 00:29:50 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 16 Feb 2023 00:29:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Feb 2023 00:29:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1e78b99dd1fd1031c6513834c4b5f594fa3cec5d06cdeb4b65ee104180bc0d4c`  
		Last Modified: Thu, 26 Jan 2023 20:44:53 GMT  
		Size: 62.3 MB (62341068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfd36dfebc232a4f5bf45dbc71ccf768dfdaaac49a08bfd23f83263014fa104`  
		Last Modified: Thu, 26 Jan 2023 23:14:31 GMT  
		Size: 151.9 MB (151945242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2140845027fb2286cca1095551b3c176f610c35d529bc03caf80e4c815def3c9`  
		Last Modified: Thu, 16 Feb 2023 00:37:41 GMT  
		Size: 12.7 MB (12719167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dfaddd2a00d117883ac47eaa5b5d40084d90cd0ce05452359e4f9154c56e84`  
		Last Modified: Thu, 16 Feb 2023 00:37:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae87f0cd3341e6bba78530b0735633b5d985b063bea3c4d5efdd084f4cc05c5`  
		Last Modified: Thu, 16 Feb 2023 00:37:40 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:372803b370b5bf59deae2c8da9615be185516dea512a6835e7d3263d2ffebb9d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227159751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26fde83e34391e033b4cfd958c8b2cf4030b0f187ed1eebde16dbede7268e51`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 26 Jan 2023 22:39:30 GMT
ADD file:1b056f516caefc99e89cee1ffa2d3b98a54ec5756d3c54b0b1c75c6ddfa9e1ae in / 
# Thu, 26 Jan 2023 22:39:31 GMT
CMD ["/bin/bash"]
# Thu, 26 Jan 2023 22:57:08 GMT
ARG version=17.0.6.10-1
# Thu, 26 Jan 2023 22:57:28 GMT
# ARGS: version=17.0.6.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 26 Jan 2023 22:57:30 GMT
ENV LANG=C.UTF-8
# Thu, 26 Jan 2023 22:57:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 16 Feb 2023 00:46:46 GMT
ARG MAVEN_VERSION=3.9.0
# Thu, 16 Feb 2023 00:46:46 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Feb 2023 00:46:47 GMT
ARG SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd
# Thu, 16 Feb 2023 00:46:47 GMT
ARG BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries
# Thu, 16 Feb 2023 00:46:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Feb 2023 00:46:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Feb 2023 00:47:00 GMT
# ARGS: BASE_URL=https://downloads.apache.org/maven/maven-3/3.9.0/binaries MAVEN_VERSION=3.9.0 SHA=1ea149f4e48bc7b34d554aef86f948eca7df4e7874e30caf449f3708e4f8487c71a5e5c072a05f17c60406176ebeeaf56b5f895090c7346f8238e2da06cf6ecd USER_HOME_DIR=/root
RUN set -x   && yum install -y tar which gzip   && yum clean all   && rm -rf /var/cache/yum/*   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  apache-maven-${MAVEN_VERSION}-bin.tar.gz" | sha512sum -c -   && curl -fsSLO --compressed ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc   && export GNUPGHOME="$(mktemp -d)"   && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys   6A814B1F869C2BBEAB7CB7271A2A1C94BDE89688   29BEA2A645F2D6CED7FB12E02B172E3E156466E8   && gpg --batch --verify apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz   && mkdir -p ${MAVEN_HOME} ${MAVEN_HOME}/ref   && tar -xzf apache-maven-${MAVEN_VERSION}-bin.tar.gz -C ${MAVEN_HOME} --strip-components=1   && (rm -rf "$GNUPGHOME" apache-maven-${MAVEN_VERSION}-bin.tar.gz.asc apache-maven-${MAVEN_VERSION}-bin.tar.gz || true)   && ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn   && mvn --version
# Thu, 16 Feb 2023 00:47:00 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 16 Feb 2023 00:47:00 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 16 Feb 2023 00:47:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Feb 2023 00:47:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f211bebb41ee40fd8a6c26d9c71d47a936d9684219f14a2679e8f57c07bb49b6`  
		Last Modified: Thu, 26 Jan 2023 22:40:24 GMT  
		Size: 64.0 MB (63964642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b913cbee33a26dc12ce5eed0d93c237af0e16f92c90a91fce67ab0eb531eaf42`  
		Last Modified: Thu, 26 Jan 2023 22:59:52 GMT  
		Size: 150.5 MB (150469506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2a2be3ea5fd8d94dbf35ceb6a71e850f8d9216e96bdc87095f42c7a9afb66c`  
		Last Modified: Thu, 16 Feb 2023 00:52:47 GMT  
		Size: 12.7 MB (12724389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c1046aee2c5d744c22b17282432a46c576c96e88084ff00b9ed605ee56569`  
		Last Modified: Thu, 16 Feb 2023 00:52:46 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad8d18047d3a9129fff429e0eb03d43f7e44cbc3be4cad52abda8bd4f6fa16`  
		Last Modified: Thu, 16 Feb 2023 00:52:45 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
