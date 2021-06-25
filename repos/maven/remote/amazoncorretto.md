## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:1dbf26ea0f1ea4a4e8bd5d8fd98bd683aaf590813787cf7fefb6fec6e06db5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:c01b13362d05e7b5624895a198c14e196c6afbdf796c9b2032847d4deb2e6358
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221755722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700ca4a9a1b6496a7111c3ac2aca81da7fbe65d3ed9ec161be584b592685e8db`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 25 Jun 2021 17:19:49 GMT
ADD file:dc851f79dbfc66e08196951041e8c856c41a3cc24b8bc27e66722210d51e87cf in / 
# Fri, 25 Jun 2021 17:19:50 GMT
CMD ["/bin/bash"]
# Fri, 25 Jun 2021 18:02:49 GMT
ARG version=11.0.11.9-1
# Fri, 25 Jun 2021 18:03:10 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 25 Jun 2021 18:03:11 GMT
ENV LANG=C.UTF-8
# Fri, 25 Jun 2021 18:03:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 25 Jun 2021 18:22:29 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 25 Jun 2021 18:22:29 GMT
ARG USER_HOME_DIR=/root
# Fri, 25 Jun 2021 18:22:29 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 25 Jun 2021 18:22:29 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 25 Jun 2021 18:22:39 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 25 Jun 2021 18:22:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 25 Jun 2021 18:22:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 25 Jun 2021 18:22:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 25 Jun 2021 18:22:42 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 25 Jun 2021 18:22:42 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 25 Jun 2021 18:22:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 25 Jun 2021 18:22:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:85ee02fe1a09b50ffaacc1e7482fdbb3e80c577256420503196fc549b9e4ef29`  
		Last Modified: Fri, 25 Jun 2021 00:50:03 GMT  
		Size: 61.9 MB (61940054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8aa833216711e402e64c17be0cc87781c22e171905ddae945991842d3dde243`  
		Last Modified: Fri, 25 Jun 2021 18:05:08 GMT  
		Size: 146.7 MB (146653843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcceb9be91621496c885ffe2c7dd4986512773742c227dbca3dfd4156c62ef24`  
		Last Modified: Fri, 25 Jun 2021 18:25:37 GMT  
		Size: 3.5 MB (3549631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1fe204833868431c941cdf8b165d7ecbf929da0ed3e7d23f07d4bc6b2e8f1c`  
		Last Modified: Fri, 25 Jun 2021 18:25:35 GMT  
		Size: 9.6 MB (9610983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceebee63cb7506aa9ea74611df3a75fcaa5486eefa50966cfd45387841ac8606`  
		Last Modified: Fri, 25 Jun 2021 18:25:34 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1727d43695624696f8ba5256307508811ba044353d20dd4fad2daf8283596818`  
		Last Modified: Fri, 25 Jun 2021 18:25:34 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f40a6a9f255e16ff866dd3dc9d0509c739234fc5fdba737364e6a36420657a32
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221505154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad262a7ee646c5333185a99acc2a2e3d20a72eecec11f7f35ab3b620eece81e0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 25 Jun 2021 17:39:34 GMT
ADD file:d4d6f883cd1ba97522a617c6f7b0125b0a82e12101c702ca57ac48063f0e3707 in / 
# Fri, 25 Jun 2021 17:39:35 GMT
CMD ["/bin/bash"]
# Fri, 25 Jun 2021 17:57:17 GMT
ARG version=11.0.11.9-1
# Fri, 25 Jun 2021 17:57:42 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 25 Jun 2021 17:57:42 GMT
ENV LANG=C.UTF-8
# Fri, 25 Jun 2021 17:57:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 25 Jun 2021 18:44:21 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 25 Jun 2021 18:44:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 25 Jun 2021 18:44:22 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 25 Jun 2021 18:44:22 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 25 Jun 2021 18:44:30 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 25 Jun 2021 18:44:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 25 Jun 2021 18:44:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 25 Jun 2021 18:44:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 25 Jun 2021 18:44:32 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 25 Jun 2021 18:44:32 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 25 Jun 2021 18:44:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 25 Jun 2021 18:44:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b19e557e673ca4274c5ee576b0d897c535e4329a596ac20b3ff70225b734a125`  
		Last Modified: Fri, 25 Jun 2021 00:50:31 GMT  
		Size: 63.6 MB (63564395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272f52eaf0f237a58fa938911ff43ad81322db0e980d569f9ef35a761e6aaf3f`  
		Last Modified: Fri, 25 Jun 2021 17:59:47 GMT  
		Size: 144.7 MB (144740675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8275dd8808cf3ca20dd44013754e1ad5b2f6231f1a455f48b21104c3794d873c`  
		Last Modified: Fri, 25 Jun 2021 18:49:05 GMT  
		Size: 3.6 MB (3587894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec519a72f89ba716543c2cb52f4311eee50f378388df7a9de58faf7fd26bd84c`  
		Last Modified: Fri, 25 Jun 2021 18:49:06 GMT  
		Size: 9.6 MB (9610981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f3e496a5642f41fe2af8d1a7b8798e678346e6591a80fe37a787d9069e16a4`  
		Last Modified: Fri, 25 Jun 2021 18:49:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0784d78f5258b26584f80e627be85f37456e6728fa1698e0b3d31bddd80bf7dd`  
		Last Modified: Fri, 25 Jun 2021 18:49:04 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
