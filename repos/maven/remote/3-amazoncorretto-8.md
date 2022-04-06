## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:424e65ae1fcc48472fd9df7e2d0caabc21eb27721bc4139753d02599259c27cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:42d34d6b4bc4c3b3f23df9499928e6e84d408a603bc8fcf8c6c23079aeabd0d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150093691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50683e35bb7e0e51ba76d38b728fe2f4d6a3d4fb49b3a30f46c5803902e27a76`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Mar 2022 05:26:26 GMT
ADD file:4e47205cb284668bcfa38b8efbacd331b3fca78d6893a1ca037e00f6f3612643 in / 
# Fri, 18 Mar 2022 05:26:27 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 00:33:41 GMT
ARG version=1.8.0_322.b06-2
# Sat, 19 Mar 2022 00:34:09 GMT
# ARGS: version=1.8.0_322.b06-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 00:34:10 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:34:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 05 Apr 2022 13:37:25 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Tue, 05 Apr 2022 16:57:32 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 05 Apr 2022 16:57:32 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Apr 2022 16:57:32 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 05 Apr 2022 16:57:32 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 05 Apr 2022 16:57:34 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 05 Apr 2022 16:57:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Apr 2022 16:57:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Apr 2022 16:57:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 05 Apr 2022 16:57:35 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 05 Apr 2022 16:57:35 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 05 Apr 2022 16:57:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Apr 2022 16:57:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:20e1cc2336fb3a7a833ea690a50980a547ab8eaf90797eccd05c4dffe60d7f2a`  
		Last Modified: Wed, 16 Mar 2022 17:46:01 GMT  
		Size: 62.2 MB (62205270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ab55b53dc663b3f49d5365e362ae8603d4eb641f1b40c6a1f292b81dec925`  
		Last Modified: Sat, 19 Mar 2022 00:40:22 GMT  
		Size: 75.5 MB (75529405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609eab19fb93f471f2ab6ca5e6213069f7e8d6e642e3c8d163f869d0956873f9`  
		Last Modified: Tue, 05 Apr 2022 17:07:18 GMT  
		Size: 3.6 MB (3621416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9401b4d5da74b9105c6b6212ec6c2e4b70f4f76fc713f0f1e9ad94cd9adc8ca`  
		Last Modified: Tue, 05 Apr 2022 17:07:18 GMT  
		Size: 8.7 MB (8736387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ea737d01536086ea0d5f0f1200b4ade5abc56f562e3b71b18e73046ba2659d`  
		Last Modified: Tue, 05 Apr 2022 17:07:17 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d173fd633ab9488a506de4e5efe7916380f4ecaf86efafb0f9cfbe010ee342`  
		Last Modified: Tue, 05 Apr 2022 17:07:17 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4cf5d8061b1676ff218daecee4bff2803ba6ef4f071dc80dba98400225bd68a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135758206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c2625a5548b4f090ddf5442c09decfacc2d62bb0b2cbb067105ff09452a2cc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Mar 2022 00:36:59 GMT
ADD file:2b2d809ac07187a252399bb24721c7a295cf5fa71ef4e526ea56bb8d1bf77fd0 in / 
# Fri, 18 Mar 2022 00:37:00 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 15:02:58 GMT
ARG version=1.8.0_322.b06-2
# Sat, 19 Mar 2022 15:03:11 GMT
# ARGS: version=1.8.0_322.b06-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 19 Mar 2022 15:03:11 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 15:03:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 05 Apr 2022 18:40:42 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Tue, 05 Apr 2022 18:40:43 GMT
ARG MAVEN_VERSION=3.8.5
# Tue, 05 Apr 2022 18:40:44 GMT
ARG USER_HOME_DIR=/root
# Tue, 05 Apr 2022 18:40:45 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Tue, 05 Apr 2022 18:40:46 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Tue, 05 Apr 2022 18:40:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 05 Apr 2022 18:40:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 05 Apr 2022 18:40:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 05 Apr 2022 18:40:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 05 Apr 2022 18:40:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 05 Apr 2022 18:40:59 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 05 Apr 2022 18:40:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 05 Apr 2022 18:41:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:16a64fa775cc87d32953ff0ed81775d6ea6b725a7946b4260298cc1ec4b5b32b`  
		Last Modified: Thu, 17 Mar 2022 02:22:32 GMT  
		Size: 63.8 MB (63828887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eea3747e3b1ed6913a6b20c1e9b7d3761b271cd757c94dd39ae0678e52e08d0`  
		Last Modified: Sat, 19 Mar 2022 15:04:46 GMT  
		Size: 59.6 MB (59564875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228b8a11be9751f5fd17d2bbbc31ec540587bdafb7d2eea6d58d2fdfd410810a`  
		Last Modified: Tue, 05 Apr 2022 18:50:10 GMT  
		Size: 3.6 MB (3626888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bd4433f0ffa23f271beee051749427d546cdae6ae5287e7c49bb93351a079f`  
		Last Modified: Tue, 05 Apr 2022 18:50:11 GMT  
		Size: 8.7 MB (8736339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3956f1d560d64ec5f2ed5ffc106041f0aa0702166c5118f8eacdadb533851`  
		Last Modified: Tue, 05 Apr 2022 18:50:10 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c1a96251b74d47edad9bcc459a9169c6e5a5764952ba6c5b85228a676fc1b`  
		Last Modified: Tue, 05 Apr 2022 18:50:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
