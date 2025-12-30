## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:1cb4af17f616e80413dce4d137def768659bc13f504877427b2dead25ad4a93a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:ee18dfdf9e9053c1cfd2644f6871f5f83ee802b8b83d91a1d47cca6a896af0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240574951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8714a3a2496219ce346f24eb90191e45bf0d0e6eef470f47609bc2116d57c2db`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:10:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:10:28 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:10:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 30 Dec 2025 01:10:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:10:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:10:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:10:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:10:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:10:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:10:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:10:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:10:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:10:28 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:10:28 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:10:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:10:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:10:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada1b757923333602be666961b075c12bc2fd99aed64a846fca830276f7eaf6b`  
		Last Modified: Tue, 30 Dec 2025 03:30:21 GMT  
		Size: 201.5 MB (201485133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c888ce8369e47cfdb27ac54078ba3e64587ad78b423fd071e4306c1f1bc21`  
		Last Modified: Tue, 30 Dec 2025 01:10:59 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b889dc0a74481a576d48a11a11664e519c3a1bbcb2eb4fcc7aed38f694851f74`  
		Last Modified: Tue, 30 Dec 2025 01:10:58 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802d077365e288c360acaee23b0efb2d33ca8062aea24b58d43b56745c9e850c`  
		Last Modified: Tue, 30 Dec 2025 01:10:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:200df8e175f65786ed2078830c6e4857df254e8c18451b2545d5d6fa36b0efc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d58522b3b4e1cafe7733414a77f1ab0c5fa2ae2ae8e6ff04d58305c6512daee`

```dockerfile
```

-	Layers:
	-	`sha256:5d9d2ec52f0f4c3522be96a99cf801feefa34b1d1a9547c435bdef7b8de7d9a0`  
		Last Modified: Tue, 30 Dec 2025 03:28:42 GMT  
		Size: 3.1 MB (3103965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfe7dc904cb0af05033c8cb7e7c8bebe0b5fc08f1900f52da99a7ba775dfefc`  
		Last Modified: Tue, 30 Dec 2025 03:28:43 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a734c6846e12967e63b3ca8359e09c419ad5efda06ec2924cb39dc18b0076af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239377495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113b35c068c4339df916fe438b1590b6cc1d1e05132a37ea64303c909c8507d0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:11:42 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 30 Dec 2025 01:11:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:11:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:11:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:11:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:11:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:11:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:11:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:11:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:11:42 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:11:42 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:11:42 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:11:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:11:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:11:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfdc6aa0bcf1d1978097fbe7d09ee2db00227b9fbe008497137c1e44d7c7f2d`  
		Last Modified: Tue, 30 Dec 2025 03:35:07 GMT  
		Size: 199.9 MB (199925576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1a92620b59d43ced71e7f3b2068048b8a1940c698b73192555135e992ae830`  
		Last Modified: Tue, 30 Dec 2025 01:12:13 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff4b057c4cac1a635171e96a2e640d0a575791e462957c2f75ba98a10efe515`  
		Last Modified: Tue, 30 Dec 2025 01:12:12 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1fdfc7e97970c5f75cf37948a9d52964c65c7dc66380ce9b6b62431546ec95`  
		Last Modified: Tue, 30 Dec 2025 01:12:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:e1ed9654f9cee7b45b907b1644ef248c892a44676c3261d54f5d0f7de837777e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512fbe7228d7c5904c0521facac9b49fd19048ac1baf399e7c681c3c4b49a19c`

```dockerfile
```

-	Layers:
	-	`sha256:7c3cf7dad9412b9a7d95e3519e634e771b2d3dad240469be93b8a121e701e7fd`  
		Last Modified: Tue, 30 Dec 2025 03:28:47 GMT  
		Size: 3.1 MB (3103628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81dacd34d95aa6deb96f2db4199fb4d244615ed480f4ff1010bde0ae4136bf15`  
		Last Modified: Tue, 30 Dec 2025 03:28:48 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
