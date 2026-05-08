## `maven:3-amazoncorretto-25-debian`

```console
$ docker pull maven@sha256:3376620aea3b08b9caab617d49e36616af3da862d0f864c95e8d666f1db47870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian` - linux; amd64

```console
$ docker pull maven@sha256:acde540ca5e37549a98f5664f8b17038340a597c771782d953f315c1f788aa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274636786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8423f47520452796806876a32581d44648a00f1632f40dc89f5b9185495963e4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:23:17 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:23:17 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:23:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 22 Apr 2026 02:23:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 02:23:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:23:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:23:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 02:23:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 02:23:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 02:23:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:23:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 02:23:17 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 02:23:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 02:23:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 02:23:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868c741caf37d188f63e9aebcddef8e80b7ba06530b274c72db237b1377db321`  
		Last Modified: Wed, 22 Apr 2026 02:23:42 GMT  
		Size: 235.5 MB (235543411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2f7b591acfc5213e50b93971ad45db14249cdc77082ac431dff73fde8d955`  
		Last Modified: Wed, 22 Apr 2026 02:23:36 GMT  
		Size: 9.3 MB (9312197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621a364b11aa57648049e2db165db850698f9b947a3e7602f03edf4ca58e645a`  
		Last Modified: Wed, 22 Apr 2026 02:23:36 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53980d8e7a44ce0b1443045a1c5c7d940cb7f743e3ae0bd0f17ce3ebef6815a6`  
		Last Modified: Wed, 22 Apr 2026 02:23:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:6004f559e4bde0a2fa089373f2bbb3bd3160b802847345cb18a0729ee5132432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a3f309518b2ca7ff2ecac9eaf0695c55f6116bdaca465962be8c10ed477f12`

```dockerfile
```

-	Layers:
	-	`sha256:3093b530fb3ccc93d00f9f82b32926de283cf3232f7d0c0d880d3f701e2be309`  
		Last Modified: Wed, 22 Apr 2026 02:23:36 GMT  
		Size: 3.1 MB (3113732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb9edeaae14cdf3a932ae98f6163216485a35fa9e111dac24383da7134f6280`  
		Last Modified: Wed, 22 Apr 2026 02:23:36 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:980bf6e05a28ec47706999f1f0c7896b9b65a1b977e92744468592f3167596f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272737871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509c74fb3fe75bfaf011f9397f882c74ce237b9a9c70759fbf6f8cf324da6390`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:30:18 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:30:18 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 00:30:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 08 May 2026 00:30:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:30:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:30:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:30:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:30:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:30:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:30:18 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:30:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:30:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:30:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca7a0e7f962ff6787d8b2689316d143cfb49ab7d1937a4c411eba558e2b66e7`  
		Last Modified: Fri, 08 May 2026 00:30:46 GMT  
		Size: 233.3 MB (233281013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c7935edb69515fce29d12f5d0cdb06119132827d37925b1f08b0fadf1149b`  
		Last Modified: Fri, 08 May 2026 00:30:41 GMT  
		Size: 9.3 MB (9312249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16af917a565219bb9fe255d3c0e275e548e5068c514d4ee3cf15e4baa0908ea`  
		Last Modified: Fri, 08 May 2026 00:30:40 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46037badec59752fc45c8a6c630a18b06d1e403aee1775a90fb7cacbb357d89`  
		Last Modified: Fri, 08 May 2026 00:30:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian` - unknown; unknown

```console
$ docker pull maven@sha256:cb92d93fd1ab52686b1b3a0904c64ff8aa8c488fa5d0032b3e0cf1f8d9ebc0ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a611d9ca1a2bf321c8d94b578c9251873a81570feddad95393b7c32d6cd33d11`

```dockerfile
```

-	Layers:
	-	`sha256:75e1674302b6e22d39a2fe3ed7313b751b9ce2aa5bd5efdcac24af8b832a53a9`  
		Last Modified: Fri, 08 May 2026 00:30:41 GMT  
		Size: 3.1 MB (3113392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd97385483d76d139890dd72f4f60870a379294389bf795b81d20a5064202ec3`  
		Last Modified: Fri, 08 May 2026 00:30:40 GMT  
		Size: 17.8 KB (17847 bytes)  
		MIME: application/vnd.in-toto+json
