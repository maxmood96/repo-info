## `maven:3-amazoncorretto-8-debian-bookworm`

```console
$ docker pull maven@sha256:6891741c08f034b26ca09875fa0b1c5472d2389b78dce27bf22bb34752ff8691
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:e7402c7c74137bbede5f7fbc36b9f30e77b57364c749e9415ecd48eff731ebfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163596885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ea30fad0a757f63e2582e94ad5154f01e723fa36570a0cd15c97317276398c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd9da9ea4671a89d6980c795da6aebe26fa443f8cc665b4ac0f8887dfcef551`  
		Last Modified: Mon, 27 Jan 2025 20:20:59 GMT  
		Size: 126.2 MB (126213000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ccad67cebba3c6629d0d1bd17dc1a0297bf5a6caf35c5fbedb0ecf5df54488`  
		Last Modified: Mon, 27 Jan 2025 20:20:57 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8164764e42616127d7ced5fddf5f7676c8b2c3707fb32b74d2f6f4ec109ef44a`  
		Last Modified: Mon, 27 Jan 2025 20:20:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606470663ab0737a45efa6437861b554f10e71d5597e93a162a1dee75d242bdb`  
		Last Modified: Mon, 27 Jan 2025 20:20:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:4600e30f46976696b8eb58aed9b82948b61540df0f182988b795300dc21e6a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f201ff8246d03186ad40969d37ab1d1c1bb215b2670987e5cf88a18dcd81a0`

```dockerfile
```

-	Layers:
	-	`sha256:31ee10050d71e423fca834a059485492ceda87d9547ddabf1b71c70b622bc531`  
		Last Modified: Mon, 27 Jan 2025 20:20:57 GMT  
		Size: 2.9 MB (2873803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31a07f1c6a2688c284a35c8fcf1b124aa486d7a9217397c3ab0f6669d75abc0`  
		Last Modified: Mon, 27 Jan 2025 20:20:57 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8ad9f71c2792540c24d28d439a1efcbe7943de8475d4f3251a122418ae13304b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147206596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b481010c4e1557120265bc8f2fcc949816d93d758b880ff50b908b5d097efd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e552bc6344f9c0296cc9fcdee38a6b8c69ef74ea312118cfc97018abfe823497`  
		Last Modified: Mon, 27 Jan 2025 20:24:11 GMT  
		Size: 110.0 MB (109994092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596233958681f84eb94a09e9ce5b564299127373fc718e828a8d39d3eb176801`  
		Last Modified: Mon, 27 Jan 2025 20:24:08 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d86b2b6e8b4c20ac94a56f0280236236951fdfbc64b837c8f24764eecd1484`  
		Last Modified: Mon, 27 Jan 2025 20:24:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd71a04439e9a4b393e58b6897954544cdfb1ecf1f01a23300159fb1d62e548`  
		Last Modified: Mon, 27 Jan 2025 20:24:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:f50afb4bc0624f9bfb5d6267a0f3097d3bd41ef7a0ead9652da469ad9650c53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a47dfd18d3db7caa9b53ac40dcd770649cbac505c5a128b3a78d662521ab01`

```dockerfile
```

-	Layers:
	-	`sha256:8e0a2ac436c874de2a5deb91431739b297b9f32239dd9a55ffff206e206b7954`  
		Last Modified: Mon, 27 Jan 2025 20:24:08 GMT  
		Size: 2.9 MB (2856621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105412565d102c29f512cff8a568fee2d565a299bce1ad2c7f76db56f8048a06`  
		Last Modified: Mon, 27 Jan 2025 20:24:07 GMT  
		Size: 19.4 KB (19394 bytes)  
		MIME: application/vnd.in-toto+json
