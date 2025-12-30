## `maven:3-amazoncorretto-11-debian-trixie`

```console
$ docker pull maven@sha256:9c270a276d5f9ce5d562fc9d56bae58794d97b11b8f44fb79d9fa52cee28cc97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:25fece0c8cd67eeaa4ed9afd31450e91e72f99e5183b27973d452bbdaf833c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241678823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b9d7d3545977cd88c3cbd5674a1643d275c666c325556b2592e663d4aec793`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:09:59 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:10:00 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:10:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 30 Dec 2025 01:10:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:10:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:10:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:10:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:10:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:10:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:10:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:10:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:10:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:10:00 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:10:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:10:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:10:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:10:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc23edeb51067e6fef48d0627aed42ac41a5b88b6a46ff2204bcb5391077edfc`  
		Last Modified: Tue, 30 Dec 2025 04:41:56 GMT  
		Size: 202.6 MB (202589017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaafefbe211c3e81822d8ef1cf8cf01ce8578d4c3d8102d4254af59e167856d`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021881c63ac47ff7fcd0f73e88f65ee7456c8b48acb65a450cac1498174327d`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b395a557cedefa94606ace4120546ad97fe87102c4807ac483aed8a7ecb06`  
		Last Modified: Tue, 30 Dec 2025 01:10:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:aaa90228fa7ef0f755cd71fec630060aa08fecd35c9069b6fb681e02b00783d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7267a35cc3a146290767d0b9dd15e37b471847ede5178f857868511db92aa71f`

```dockerfile
```

-	Layers:
	-	`sha256:fd2c6d2ec99f7e920e9225c7462867aebf730106945fc5b4f33477e166e75ae0`  
		Last Modified: Tue, 30 Dec 2025 03:28:32 GMT  
		Size: 3.1 MB (3109756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450aa41fd3ccf19455095418a303850fa53ff6e94b20f7c8c4b63ea4d30d2e66`  
		Last Modified: Tue, 30 Dec 2025 03:28:32 GMT  
		Size: 19.2 KB (19200 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5bc48bda1b01d97f25202828f7ee0e2ce2f77544cf948e46fea10d7ebe602b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (239017979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83263354a99557fa4a710cfc03c963303ccc27c2af5d00ad130b685da6ec7da2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:11:18 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:11:18 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:11:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 30 Dec 2025 01:11:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 30 Dec 2025 01:11:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:11:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 30 Dec 2025 01:11:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 30 Dec 2025 01:11:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Dec 2025 01:11:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 30 Dec 2025 01:11:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 30 Dec 2025 01:11:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 30 Dec 2025 01:11:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 30 Dec 2025 01:11:18 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 30 Dec 2025 01:11:18 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Dec 2025 01:11:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Dec 2025 01:11:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Dec 2025 01:11:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f372a43116c4818782215daa2cb5854814dfea661f99b6c802c4aa263bd158e8`  
		Last Modified: Tue, 30 Dec 2025 01:14:31 GMT  
		Size: 199.6 MB (199566059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8219911ee009667d8d638a7be759b86586e5ee13ea7fe797817dc537602063ec`  
		Last Modified: Tue, 30 Dec 2025 01:11:51 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b3a9a8c765ea86764c8d73b652f170d98cf3e706425873e6e4f756c8190c7`  
		Last Modified: Tue, 30 Dec 2025 01:11:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f43d7da352bafd93580e1189d5368ffd4a62b890ce9afbafe3de034c841c4ba`  
		Last Modified: Tue, 30 Dec 2025 01:11:51 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:7d54e95688365fef85b758060892225941ec684d9c9046272ff15644084a1b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db974b5723d60d5e2d486bdd94404fe7d73cc0db477b048fa8a72cd107ba7c6`

```dockerfile
```

-	Layers:
	-	`sha256:ec4136f0f5f1fce9a2660bd20f72a4006c25efb70a669d69d1ac6e64c4aff8b2`  
		Last Modified: Tue, 30 Dec 2025 03:28:37 GMT  
		Size: 3.1 MB (3110056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812ea0a16e357a92a3e3c049e0583dadbcedfd42aaae7fdc33356a5cdaf738b`  
		Last Modified: Tue, 30 Dec 2025 03:28:38 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
