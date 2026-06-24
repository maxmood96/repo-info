## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:aa2abb1116b011913255890a544f068bcd75fff86bcac6ea4679d684aa414cfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:40bd55dd5d11f9bd3e7184410e9224393942827c229da5327595e66fd763a472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256025946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5070885ffcb07fd737f5959dccc6a668d80b20f117dd15d1bf4442968d3af6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:24:40 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:24:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:24:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 24 Jun 2026 02:24:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 24 Jun 2026 02:24:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:24:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:24:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 24 Jun 2026 02:24:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 24 Jun 2026 02:24:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 24 Jun 2026 02:24:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:24:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 24 Jun 2026 02:24:40 GMT
ARG USER_HOME_DIR=/root
# Wed, 24 Jun 2026 02:24:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 24 Jun 2026 02:24:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 24 Jun 2026 02:24:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bccc338d627825a33f3f80782b65241030429079a8ff92c7823232c9fd756e0`  
		Last Modified: Wed, 24 Jun 2026 02:25:04 GMT  
		Size: 216.9 MB (216879558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e3540885f5addb348301cd201433bf940b8ae382e5eed779b77dc46fd242d`  
		Last Modified: Wed, 24 Jun 2026 02:24:59 GMT  
		Size: 9.4 MB (9359964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bf937613dad72bd203b223293ba3cd63491ed580231a1e2adf22122ca2733c`  
		Last Modified: Wed, 24 Jun 2026 02:24:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fde6ae5b579cd7423f3d7b5c6e883e98fc81c7ba7520e984eb08b10e2387f9`  
		Last Modified: Wed, 24 Jun 2026 02:24:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:51d1d2ead170d81a6da039c40229bc3ef5d5097c76788be0d5f6d3e49294d160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca8fe0cdf0ffa5f070c1bbbb8ff9e06c5e19f43afc777f207fe34d3e020f0e0`

```dockerfile
```

-	Layers:
	-	`sha256:69b83a7eaa8f1af22a18ab08f2c0a12e831146c72407066c786bafef7ae2b988`  
		Last Modified: Wed, 24 Jun 2026 02:24:59 GMT  
		Size: 3.1 MB (3104789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a035c4c897344832074990628d1b18ce42e7dce714c6392b68c416af4ac6b0ef`  
		Last Modified: Wed, 24 Jun 2026 02:24:59 GMT  
		Size: 17.5 KB (17524 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:53ac77bbccd4ec50b425850f7ea3505361f8a8358a05fc46173674b4780be361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 MB (254439010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99914ed2151300808b0fb8acaf2c338aa8072fe058f271a094d183930658afe8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:31:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:31:06 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:31:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 24 Jun 2026 02:31:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 24 Jun 2026 02:31:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:31:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 24 Jun 2026 02:31:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 24 Jun 2026 02:31:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 24 Jun 2026 02:31:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 24 Jun 2026 02:31:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 24 Jun 2026 02:31:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 24 Jun 2026 02:31:07 GMT
ARG USER_HOME_DIR=/root
# Wed, 24 Jun 2026 02:31:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 24 Jun 2026 02:31:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 24 Jun 2026 02:31:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a739071a5043a1d9713daa00fcd98f1c03cd88c970dda9c2f01bc977185de1e4`  
		Last Modified: Wed, 24 Jun 2026 02:31:35 GMT  
		Size: 214.9 MB (214929484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8808d5526f06ab09dc37d8e0c9567e776910bca521a5160b9347f3feba0abbb`  
		Last Modified: Wed, 24 Jun 2026 02:31:28 GMT  
		Size: 9.4 MB (9359970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ffdb190b1451264b94c6320e7ca4cc08c3d080da21dc63cd5885b9be1516b5`  
		Last Modified: Wed, 24 Jun 2026 02:31:28 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a51a3cb8bf4cb69283ea0c80f7edb79117635c9dc5ab0a64543da51a7f1ec1b`  
		Last Modified: Wed, 24 Jun 2026 02:31:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:0f0f58c45e3071b9c587a78ab1e55f7d4cdfb87a746cb3ef7b41abd3ce961fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457d4bf5e21dd1f78125eaee29d7849e454161f03d6511d95b345e47887e7488`

```dockerfile
```

-	Layers:
	-	`sha256:a2e5ce6f82d35cac134b85f92fd3e27a86e72d4c3a138a37182bea4564972b4a`  
		Last Modified: Wed, 24 Jun 2026 02:31:28 GMT  
		Size: 3.1 MB (3104444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12873d1c1619a493d2acfe01cc9db30110d12aee81cc774313c32802deb74afe`  
		Last Modified: Wed, 24 Jun 2026 02:31:27 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
