## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:426336fcc5582335affbf586dd0c723f9289739b61270e09ccb69fe683dbe09a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:7fba9a91b0325674c16f0b740bd6abc735a6d80043b3d029d9ff1eabe6eb5f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164466310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5caab28f1737ffe02dd74d394ffb4df864aa7be24844edc7ff71eb3a7a16bb7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1aa863c8fac3a4c86f4b3699558561b6cad21dd1ec36c1de7676a59364eb48`  
		Last Modified: Tue, 17 Sep 2024 03:02:58 GMT  
		Size: 126.2 MB (126168347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c0fd92a97378ec921b9f4e7c46edd190763c1b96372101984ca6201447a2a5`  
		Last Modified: Tue, 17 Sep 2024 03:02:54 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b5ed21eb4ec0f2a6670874ec4feab6ddf04366e1fb20b75c72345b60d672aa`  
		Last Modified: Tue, 17 Sep 2024 03:02:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cc2e25a8ff6a13215e3196ca51147be7cda2de821934e6585c7137390c2eca`  
		Last Modified: Tue, 17 Sep 2024 03:02:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:4595735a34d078315ea0e2ef2f1f929f9f8d8338d7fc9e472b4aefd88b1c1067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba9aaec3d621716d1f728d464521eeb0dfb9cc2c03fd766a015183227bfff29`

```dockerfile
```

-	Layers:
	-	`sha256:02ce7299b44310f0757b35bbd5904288d5a41fda3c205f1ffeabb9449b3de39e`  
		Last Modified: Tue, 17 Sep 2024 03:02:53 GMT  
		Size: 2.9 MB (2859237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664566d9d4bbff46bc48ccead2e1f13d87115afa18e392ef37def69c8432bfae`  
		Last Modified: Tue, 17 Sep 2024 03:02:53 GMT  
		Size: 18.5 KB (18496 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:29aeefcffc6127e759c9c589ec70b95c6116834cfdcb3a8bd0022be168d8cb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148260851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17be198e8042a6ca22cc75807f4682b59f8b347f5ed0f935baeb6130cb1cb4e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83946f317539b76c66ae82117a4b59042e098654b776e0c049cea724d0dbc4e0`  
		Last Modified: Tue, 17 Sep 2024 09:52:03 GMT  
		Size: 109.9 MB (109932820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65834218c75e2389ea25d125201f9cf48ee61688fab0a82542ed323fb57a5e98`  
		Last Modified: Tue, 17 Sep 2024 09:52:01 GMT  
		Size: 9.2 MB (9170448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe39df45556c1573fe5130d4c0e26177d359aa95b890cf8314d037f33b03f11`  
		Last Modified: Tue, 17 Sep 2024 09:52:00 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a6a577088715832d28dbc745468e0f2b28a7b75a9e561cf71a651e1cef7d19`  
		Last Modified: Tue, 17 Sep 2024 09:52:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:da3d2b69f21a549e5d4cb7ecee789d886197befc555a307128d276877f52fb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2861284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c1334fcd73ca0e074fba69c0276139521aee31692fed7be9fda6980a37fd94`

```dockerfile
```

-	Layers:
	-	`sha256:aeced363f7a1316f146d6a9f9812f9d37e02ef11b0610cf4e7887443232a3b81`  
		Last Modified: Tue, 17 Sep 2024 09:52:00 GMT  
		Size: 2.8 MB (2842103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa3b15e33c60af0b7bc21b1081239af0d70b7adec01dbd11107fc0b126b5b36`  
		Last Modified: Tue, 17 Sep 2024 09:52:00 GMT  
		Size: 19.2 KB (19181 bytes)  
		MIME: application/vnd.in-toto+json
