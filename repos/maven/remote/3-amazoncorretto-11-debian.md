## `maven:3-amazoncorretto-11-debian`

```console
$ docker pull maven@sha256:410968fef204d5701c539bae825cd0d56ac1f414feb253461500f12677c4de83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian` - linux; amd64

```console
$ docker pull maven@sha256:9eeb228ae80d52c15b4bd374db4143a49bc30d29bd24ba86ee7d34a9184d3258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244705846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14dd3c552246ee9dc7d3dfb439a79eea9fb8cf0317584da2c0f24b520a828ea`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 18:11:50 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:11:50 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 18:11:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 21 Apr 2026 18:11:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:11:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:11:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:11:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:11:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:11:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:11:50 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:11:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:11:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:11:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791aabf66c6075bc6ecf6a0b7cf073b91ae02afd7fa05b75d0e9649f2adc9506`  
		Last Modified: Tue, 21 Apr 2026 18:12:16 GMT  
		Size: 205.6 MB (205617004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5819297d01385dbee6a1131b1b712f8b5a2f99499d19b408fa81358ea715895`  
		Last Modified: Tue, 21 Apr 2026 18:12:10 GMT  
		Size: 9.3 MB (9312196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e3c17e05d50809b648e626e7cc169bc8e45977e2a76b80c5a00a1110dee090`  
		Last Modified: Tue, 21 Apr 2026 18:12:10 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780f587884577aeea8219c039f360a1876a14596ce23f5a29051504d0df32bf2`  
		Last Modified: Tue, 21 Apr 2026 18:12:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:9a409d6f7773291a47f31020764e743e626c7a92204163523a669915fa12e5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83c44f510415db239fd35df70585a56c0811bbcf5220878dfdc9f8d55d5cd84`

```dockerfile
```

-	Layers:
	-	`sha256:d91c94545b07fddf2a8f34798861c19b1d9f8b6b0dcb23030e34445196a13075`  
		Last Modified: Tue, 21 Apr 2026 18:12:10 GMT  
		Size: 3.1 MB (3109880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6fb52cb0c0afbe9b45c6f1891dbaf56ef974aae0deba52125fd3b3b9180ec77`  
		Last Modified: Tue, 21 Apr 2026 18:12:10 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3946b227cb2c149e8ff13592f44db355c3eb6e6c9fe6f2a23bb00160d51fcf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239269148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672cea95d695211330c3c8a49ef953486d2391e391cc5265c732d34e63b31264`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:25:53 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:25:53 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:25:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 22 Apr 2026 02:25:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 02:25:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:25:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:25:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 02:25:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 02:25:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 02:25:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:25:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 02:25:53 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 02:25:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 02:25:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 02:25:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db554f8da5c26d4aad3260ce2acd1d4f8acf9ad55b55836563077d815001a685`  
		Last Modified: Wed, 22 Apr 2026 02:26:17 GMT  
		Size: 199.8 MB (199812283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d6ae646ac592e6a60f71d9f19f63273d22454e58ad0c2f2a18eb4ede553a6`  
		Last Modified: Wed, 22 Apr 2026 02:26:13 GMT  
		Size: 9.3 MB (9312255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a8a61e20b6bec1121a371d2a09fdc2aad9c26149ecb001aaf1d3753d472a55`  
		Last Modified: Wed, 22 Apr 2026 02:26:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff2a6f5f59a8ac5471b1edb32eb5e43f28229f8fb3bf5b9e54cb47cb3dd1427`  
		Last Modified: Wed, 22 Apr 2026 02:26:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian` - unknown; unknown

```console
$ docker pull maven@sha256:4eac49befe91cc2ad13ae373fce6cfcb6bf7cbd26799a07ec5b4f9c098f68a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9400470f1811a2fec08dadb4bfd67d75918a325ebe87978349cd3aa9801c9d2c`

```dockerfile
```

-	Layers:
	-	`sha256:cae0aa22e889a69bad739e0d34b72039d0f7404174c884908c42c0b248117351`  
		Last Modified: Wed, 22 Apr 2026 02:26:12 GMT  
		Size: 3.1 MB (3110182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16bede57a87ce0a3fa15551dcced352bc3f082979e87b648fb4b7bea482cc26`  
		Last Modified: Wed, 22 Apr 2026 02:26:12 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
