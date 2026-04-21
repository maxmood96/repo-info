## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:e2e847f83e06b5dfec86d712bb00ae7e01f4c5d08068f528e1bc2cf89be8f7ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:fe623d489b631970220bca2e1975744973f04adc8d6a8ffa6c83e192e7689248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167695586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a7505d84af6951acb814b45fe32888a521634b0ad61556df6011edd5afddfb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 18:13:00 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:00 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 18:13:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 21 Apr 2026 18:13:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:01 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:01 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:01 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:01 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0472cd9181b3dc018b814cfa2f1413177dbe0d1b02e7b1b4572538044fee72`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 128.6 MB (128606743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8956a339ebfbd8d1441c66297ef04aa33abeb09f90455f812f894ad1cb1814`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 9.3 MB (9312198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ad8817a05c2c1c98d8646db0c1c98fe5aa9d4fd7f6a338ebe5d518884b6f7`  
		Last Modified: Tue, 21 Apr 2026 18:13:14 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70ca3f246ba77687cf7a96742d9c6f7c452ec00eefe4ba54c3e11db625e57d2`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:d41055a1ca265bca40881658fed1d0608590b28a79b83b6725f09e8edef20a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0498b35aad1436d3a23096747939c9e051974f27ef68628d5a3e0fcad913dc8c`

```dockerfile
```

-	Layers:
	-	`sha256:320d2647c3827a945eb2381f30ed27070f1319e51074da5df55b28d0470fa394`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 3.0 MB (2982093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e067bf879cacea778bc3617ef8d377cd1bb3e44ef8f1dea957775014208c2f01`  
		Last Modified: Tue, 21 Apr 2026 18:13:15 GMT  
		Size: 17.5 KB (17533 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7d54ca6a506bd6fb78a26bbc8a0cf061971e6d7678a04941429bc5258e58d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152145549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f9ed6e6a7d8c4a998e06124f6c26f9875832c72a5912a9c920f1ad2e555a78`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 18:12:51 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:12:52 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 18:12:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Tue, 21 Apr 2026 18:12:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:52 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48267ff9df749a13aebd405c7a3e629d1f9db303753a8b84f5346d68431f0458`  
		Last Modified: Tue, 21 Apr 2026 18:13:09 GMT  
		Size: 112.7 MB (112693748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7458937d1fc5beb9dfb38969d5e9938273f881e88269bea80971881efdbe6d8c`  
		Last Modified: Tue, 21 Apr 2026 18:13:07 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641f0f353efafdc09e7031d87ab38d131b40664d8a50f15b57080cf9d1355173`  
		Last Modified: Tue, 21 Apr 2026 18:13:06 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33134c7de33ac24a201a8c464042de7e8b95887f2b6eff441e4bdd6b33f1b6`  
		Last Modified: Tue, 21 Apr 2026 18:13:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:7a1b6d9ae94bf82ad08dcd1b25164a246d808ace1dd31f696523239e3b1d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f51fea91f7619bbf7035a453dd5c4192bc3ba084b05107c7e3ef868c8f3ea2`

```dockerfile
```

-	Layers:
	-	`sha256:fcc73d5460c356ec59ac3226876f4ebbefb3a58c9b7b5253657713b759064fd8`  
		Last Modified: Tue, 21 Apr 2026 18:13:07 GMT  
		Size: 3.0 MB (2964914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f573fe59896f5391c5fc5ff96a2c671aea0fc73927a153989d10b790e1aaaa3`  
		Last Modified: Tue, 21 Apr 2026 18:13:06 GMT  
		Size: 17.7 KB (17702 bytes)  
		MIME: application/vnd.in-toto+json
