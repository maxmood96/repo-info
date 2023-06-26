## `maven:3-amazoncorretto-20-debian-bookworm`

```console
$ docker pull maven@sha256:301146eabd5fb0deb1ce81ee1e71878493da151ad6a026384af7d8bd0e2086ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-20-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:a0dd6109574ae7b368f612fd09fbeed53d07e335c826527965d3c91122c4f867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246170194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f19a9907b30496882557edbd9208cd76fd5409789f02a55c8a9ff71e1aae26c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:42 GMT
ADD file:ba1250b6ecd5dd09d4914189d72741c2817988994e7da514bf62be439a34bdb5 in / 
# Mon, 12 Jun 2023 23:20:42 GMT
CMD ["bash"]
# Sat, 17 Jun 2023 08:38:16 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-20-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 17 Jun 2023 08:38:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 17 Jun 2023 08:38:16 GMT
ARG MAVEN_VERSION=3.9.2
# Sat, 17 Jun 2023 08:38:16 GMT
ARG USER_HOME_DIR=/root
# Sat, 17 Jun 2023 08:38:16 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 17 Jun 2023 08:38:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 17 Jun 2023 08:38:16 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5b5fe70539cd6989aa19f25826309f9715a9489cf1c057982d6a84c1ad8975c7`  
		Last Modified: Mon, 12 Jun 2023 23:25:49 GMT  
		Size: 29.1 MB (29124744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f65243f81da8b80cdc3f919ee0b3fa370bf63c8264b65d6acdc2ec664790ced`  
		Last Modified: Tue, 20 Jun 2023 22:46:23 GMT  
		Size: 207.7 MB (207729649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8826c36c4288dc7a790fd1c55f1963db2b76ec9b7dd2267e0c82346040a7c41`  
		Last Modified: Tue, 20 Jun 2023 22:46:10 GMT  
		Size: 9.3 MB (9314426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936c21b262c475ad25ac14432a8b7e2059ae34a75afee0dc8231bcdd9f7e0ee6`  
		Last Modified: Tue, 20 Jun 2023 22:46:09 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419de0dfdc463ed981daaac6484a8ba91e90371f1008308d96c8079bb2674c2a`  
		Last Modified: Tue, 20 Jun 2023 22:46:09 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30ccb640f29badae937b985484a9fa45f5f51759b3b1565b485fcbd2861c495`  
		Last Modified: Tue, 20 Jun 2023 22:46:09 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-20-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:64052d94c6856d9e897b20ce13043162a553d54aa38ae386d1a5df636b34f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244027337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8218c017140480b320ffcf0ff04c862d47c9a60ac006257bf8279280fd4f7fe9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:13 GMT
ADD file:f75c3fe22fec548b35a86a9a5802fdc97497f5d253cf630d65f13282169d3f3f in / 
# Mon, 12 Jun 2023 23:40:14 GMT
CMD ["bash"]
# Mon, 26 Jun 2023 13:48:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-20-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 26 Jun 2023 13:48:06 GMT
ARG MAVEN_VERSION=3.9.3
# Mon, 26 Jun 2023 13:48:06 GMT
ARG USER_HOME_DIR=/root
# Mon, 26 Jun 2023 13:48:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 26 Jun 2023 13:48:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 26 Jun 2023 13:48:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:95039a22a7cc3ae41d71f075e6e09e91e8da850fb5f80aba2f4a09f254520539`  
		Last Modified: Mon, 12 Jun 2023 23:44:08 GMT  
		Size: 29.2 MB (29152534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8108c0e460fbee6dfa8b535e9f853772d818038991f4f4d636985ff285c1a904`  
		Last Modified: Tue, 20 Jun 2023 23:03:15 GMT  
		Size: 205.5 MB (205545871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeabdb051763039f3e16894fbdede2c31f648e2b680a66ec1ae2a97d11abcd95`  
		Last Modified: Mon, 26 Jun 2023 21:51:56 GMT  
		Size: 9.3 MB (9327568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a089df5187373174b20af05c7c215f53698c9a82cd9c9bdf578073e051bf082c`  
		Last Modified: Mon, 26 Jun 2023 21:51:55 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388c25b16bb7f1cc10470da0b3ba4856dcd3ea0d0ef00d0e3f55f821cbe60651`  
		Last Modified: Mon, 26 Jun 2023 21:51:55 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213ba70dbaad8ae18fc1e8536e2b9f7c7f0d70088184816868505cb283b91e4a`  
		Last Modified: Mon, 26 Jun 2023 21:51:55 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
