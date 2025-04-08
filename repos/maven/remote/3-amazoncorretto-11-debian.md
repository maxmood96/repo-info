## `maven:3-amazoncorretto-11-debian`

```console
$ docker pull maven@sha256:d7ad246ddfff61b34bcdf93df633547b5f369d496fff43355c2c1592a6e34d17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian` - linux; amd64

```console
$ docker pull maven@sha256:675ee01ac3cd88109adb5f4f53608577b41ec30224105e90622b9280cfb53ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241210202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc60a2ad764ea9b042f97cef9b93d6b26fc6225f2362410f2332913a6ac038e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 25 Jan 2025 20:08:38 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd00c49d733d2afd6185d2fce4daf26c3a3daffc6d18f031e6520d1928408f5`  
		Last Modified: Tue, 08 Apr 2025 01:37:04 GMT  
		Size: 203.8 MB (203811480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d673b70adc0ced6a4547acd5b670b6cea00549659ce90700572bfe9e385ca4e6`  
		Last Modified: Tue, 08 Apr 2025 01:37:01 GMT  
		Size: 9.2 MB (9170425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb01d41108325084b9d013c949c2040d8d824ce3c803e8b8491faca3c2aeca`  
		Last Modified: Tue, 08 Apr 2025 01:37:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948c99219e95be1b40d0cb30fbf08a1544974d8b28c2c66654c3297c88a392`  
		Last Modified: Tue, 08 Apr 2025 01:37:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:0a39c6a5c1d19caa8a67544474e64acab976fd79cc5180f51199a26a9a9bd98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be86c86d6a9df6e1e5abb39ce27abd402df9ae7a23b51278c7db9db06d18293`

```dockerfile
```

-	Layers:
	-	`sha256:045d778974d7fde5e3da2fec2cfdf83cc470024c994bcb61f9a52db4ce107af7`  
		Last Modified: Tue, 08 Apr 2025 01:37:01 GMT  
		Size: 3.0 MB (3002346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ac8839460e0759e99affad60cfcd6cdd7606a60609a140112ef519cb9dc8489`  
		Last Modified: Tue, 08 Apr 2025 01:37:01 GMT  
		Size: 19.2 KB (19213 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3fade826cda8c449cd3c9b8a609b138e410257f7f584bb3ec8ce149486b23850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237832483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631850c58f72da550184f81a03bf31b521e6ba8d6682335396ca7c3c78012ca`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 25 Jan 2025 20:08:38 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d3e3733882f3a1e56003d672dc2bbfd2f4eec3374b6402ebf623512da8fd5`  
		Last Modified: Tue, 08 Apr 2025 11:43:08 GMT  
		Size: 200.6 MB (200594688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61536d5b3dc84b127e5024b65573431571b5f4578199dd9f88ce41559dd8ff17`  
		Last Modified: Tue, 08 Apr 2025 11:43:04 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983fe05621626640d6fba70b4d9960207d50c3add18ca8ed06c1563a51e3bcfb`  
		Last Modified: Tue, 08 Apr 2025 11:43:03 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb854dd7d8f1d6f3874067b88821b9537289b8cb88e64cad925a72d14585e424`  
		Last Modified: Tue, 08 Apr 2025 11:43:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:5ca966301073275c784e2020ae055066840d6bf9230ca04adb8088ef4b8fea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3022025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34823d199d02d9d88ecd0ceb3f7fe2859c3a5148f5102071651ba32381082487`

```dockerfile
```

-	Layers:
	-	`sha256:10f019d1cfc9874a94120921d7ddf0312e92e245887ddd730b0a26127659bdc7`  
		Last Modified: Tue, 08 Apr 2025 11:43:04 GMT  
		Size: 3.0 MB (3002643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cb181fe4cacbc7804cae2c04725840364ab6b561ce82ac230e8ea702247f632`  
		Last Modified: Tue, 08 Apr 2025 11:43:04 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.in-toto+json
