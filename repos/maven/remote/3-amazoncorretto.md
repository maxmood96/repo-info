## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:6d7236a49b60e1beb5b9dd7354b01f535f50a638a0e354fb24c00443fdf19fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:fd0ccd6be76c0cf2221f6393463435991877cee921350f79e1c58847f6a6b413
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222416214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2818d93248ac5a926102292afce760fb75100b78436e56ec7fb8137864cfd03`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 22 Sep 2022 19:19:21 GMT
ADD file:99847692b0f2dee43b50f306ad92fbc13ccb0541af21c6d3040f72d3184aabac in / 
# Thu, 22 Sep 2022 19:19:21 GMT
CMD ["/bin/bash"]
# Tue, 18 Oct 2022 23:38:09 GMT
ARG version=11.0.17.8-1
# Tue, 18 Oct 2022 23:38:31 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 18 Oct 2022 23:38:32 GMT
ENV LANG=C.UTF-8
# Tue, 18 Oct 2022 23:38:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 19 Oct 2022 00:10:48 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 19 Oct 2022 00:10:48 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 19 Oct 2022 00:10:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 19 Oct 2022 00:10:49 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 19 Oct 2022 00:10:49 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 19 Oct 2022 00:10:50 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 19 Oct 2022 00:10:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 19 Oct 2022 00:10:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 19 Oct 2022 00:10:50 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 19 Oct 2022 00:10:50 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 19 Oct 2022 00:10:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 19 Oct 2022 00:10:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e80285ff599e329e689e4689be05885456823b7f6233486aa419541ae8e98c62`  
		Last Modified: Wed, 21 Sep 2022 22:07:12 GMT  
		Size: 62.3 MB (62303269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5503b740cc3894c1365ab7c1019b198e1cf97383bed1f539b6f7e08addbf4121`  
		Last Modified: Tue, 18 Oct 2022 23:46:56 GMT  
		Size: 147.7 MB (147745183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb23ccf1e8cdcefad7ee2eb9ec08c7c28b3139973e00715cecfabae7b9c3fadc`  
		Last Modified: Wed, 19 Oct 2022 00:13:54 GMT  
		Size: 3.6 MB (3627049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95543c91225033a575b335bfb18a8b9975bc057557adb20428dac2b3bb2cd09c`  
		Last Modified: Wed, 19 Oct 2022 00:13:54 GMT  
		Size: 8.7 MB (8739502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95de2c079350a59d9f54197457b9654b8a64176971555666967e2e616cb0921c`  
		Last Modified: Wed, 19 Oct 2022 00:13:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bfd7f1dc2f79dab1cf03f4fd34709239b0a489dde2233133091003a7fa5a40`  
		Last Modified: Wed, 19 Oct 2022 00:13:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:62d8e01feda5b8b7ca0ffe1310997899d6966894eee22a6e88bf9cf76f0b9b10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220837273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0104e5e8c44b702dcd6a138c65a327a314d9142d09f275ba97f963977827e497`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 22 Sep 2022 19:39:26 GMT
ADD file:cd0852de8cdfb2b7efdaa53ad4827a33302d895b10306b540e7df9d8c7f00637 in / 
# Thu, 22 Sep 2022 19:39:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:57:08 GMT
ARG version=11.0.16.9-1
# Thu, 22 Sep 2022 19:57:22 GMT
# ARGS: version=11.0.16.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 22 Sep 2022 19:57:22 GMT
ENV LANG=C.UTF-8
# Thu, 22 Sep 2022 19:57:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 22 Sep 2022 20:46:44 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 22 Sep 2022 20:46:45 GMT
ARG MAVEN_VERSION=3.8.6
# Thu, 22 Sep 2022 20:46:46 GMT
ARG USER_HOME_DIR=/root
# Thu, 22 Sep 2022 20:46:47 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Thu, 22 Sep 2022 20:46:48 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Thu, 22 Sep 2022 20:47:01 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 22 Sep 2022 20:47:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 22 Sep 2022 20:47:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 22 Sep 2022 20:47:04 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 22 Sep 2022 20:47:05 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 22 Sep 2022 20:47:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 22 Sep 2022 20:47:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f5371f42f94d8ba2c9559448b8e36de82d246f179760ec911f594632d3545611`  
		Last Modified: Wed, 21 Sep 2022 22:07:11 GMT  
		Size: 63.9 MB (63912418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec71345c209b6d30fbd90ce6a341d2acf9e73553f4fd336758c8c94885007736`  
		Last Modified: Thu, 22 Sep 2022 20:00:06 GMT  
		Size: 144.6 MB (144551343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e5e37def3b09a3ca0def49a6b9776ba00a64b16cba2c6c594e49ae0c5ad7d4`  
		Last Modified: Thu, 22 Sep 2022 20:51:34 GMT  
		Size: 3.6 MB (3632829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943455e09451305ceb6955faf2625613d6d3cd6ce11d5d4b66d42cb7fd213326`  
		Last Modified: Thu, 22 Sep 2022 20:51:35 GMT  
		Size: 8.7 MB (8739469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fd3da5aa24aa1f638e5a62a8122eccd0306f9edf33346bcb579e34774d9acc`  
		Last Modified: Thu, 22 Sep 2022 20:51:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b5fbb5b106c76717af67ad7f29df31616bcd5086c3910b6a0dd5365c18a737`  
		Last Modified: Thu, 22 Sep 2022 20:51:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
