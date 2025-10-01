## `maven:3-amazoncorretto-8-debian-trixie`

```console
$ docker pull maven@sha256:e88a72cc13114df3656de0f95a1cb60669b0930a4b430621d2fe59c35d7537e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:4d79e8c8691c097639920f2b5e192d2567a7d2cb9b77bc93a850fce4cd707a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164179042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e4854b8d3a944777d2fe5f27e9c2352f8934e7d851a7aa61075609b4984abe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 20:58:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 17 Sep 2025 20:58:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 20:58:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 17 Sep 2025 20:58:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Sep 2025 20:58:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Sep 2025 20:58:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb26ff1f960468b4c6af87ccfd9e1dd63852ecb479c00d2453ff6f10cb96a726`  
		Last Modified: Tue, 30 Sep 2025 00:58:27 GMT  
		Size: 125.2 MB (125157672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488bbdac29e17675141d711b28efc39c48f20f407b706d93a2acf52ca2ce5ffb`  
		Last Modified: Tue, 30 Sep 2025 00:58:12 GMT  
		Size: 9.2 MB (9242568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4f3ca0afc70c50530c65ea40e1c34a1783320729c49d40bf44e12a2037acd9`  
		Last Modified: Tue, 30 Sep 2025 00:58:10 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171ac7fdf3af3206f9da6fd5173c4cb4f726c28510e013f268903025524eae65`  
		Last Modified: Tue, 30 Sep 2025 00:58:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:abfdde42eb5599658cc946df31a0874036f019520a69509b4ee57843b173fb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b924b6bb197734c852c3d9671623b7dc531a04884a1e9619cd37895ef151e92f`

```dockerfile
```

-	Layers:
	-	`sha256:a0c9c6b725870eb5b1c01485107e76aaf657e1f19ef10396ee7ee3ff97ef6204`  
		Last Modified: Wed, 01 Oct 2025 14:27:55 GMT  
		Size: 3.0 MB (2979999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f47999a9ad959220ac55ea1e393262adb156f01dc848e72504373d744c531b4`  
		Last Modified: Wed, 01 Oct 2025 14:27:56 GMT  
		Size: 19.3 KB (19255 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:39ee154a8a45b1ac94a4b925061805c7b5fab130d1ecae526ada1ce20afb3c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148482750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fc94a37434662e98f844f7dcca46614453ef0db9abd39c8328f74603b01e80`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Wed, 17 Sep 2025 20:58:48 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 20:58:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Sep 2025 20:58:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Sep 2025 20:58:48 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 17 Sep 2025 20:58:48 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Sep 2025 20:58:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Sep 2025 20:58:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Sep 2025 20:58:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adeec2a4a5eced56eaf7191c6dc2baeb4669f702524746bc3ccecd56d96835f`  
		Last Modified: Thu, 18 Sep 2025 21:43:58 GMT  
		Size: 109.1 MB (109102499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a76cffa519c67f5a1d530e8b6ee1fba90cbd3723c2294afd684a6d8dfaec0`  
		Last Modified: Thu, 18 Sep 2025 21:43:48 GMT  
		Size: 9.2 MB (9242580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0d3aac026b86ec03106b17e6bb97e8ae01dfe8bfde53048aba84a121dfe3b5`  
		Last Modified: Thu, 18 Sep 2025 21:43:47 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819ab38661d2a6eeb4a008c42a3e313e57999b3766ef262d85f1959e4936c970`  
		Last Modified: Thu, 18 Sep 2025 21:43:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:70acca86193bbc84e1416d5b678de8f6430f2fe15c10b2e8568d691d35b518c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245b2ae6b6c8a24b5c142d3193bf96025b1e5f320aad88114ac4e0ea6da9e30f`

```dockerfile
```

-	Layers:
	-	`sha256:801193b5961983750d89989096bf071eff0eb20c4d798bb5dbb5e61474e8d449`  
		Last Modified: Thu, 18 Sep 2025 23:28:16 GMT  
		Size: 3.0 MB (2962820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444a85e5d1c8a34b2f12637c0d40f5c0892410d86e7af6b6baf5adf7f85fde44`  
		Last Modified: Thu, 18 Sep 2025 23:28:17 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.in-toto+json
