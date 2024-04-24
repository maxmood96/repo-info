## `maven:3-amazoncorretto-11-debian`

```console
$ docker pull maven@sha256:9ae125fdb359cbdb6736167735c3ce66ad6b15e4ffece32e8736726ade4f3627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-11-debian` - linux; amd64

```console
$ docker pull maven@sha256:cca290a01e2565b5b25ea4c31d4700ba04986b4147528881dbf1f1f10559f87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238179233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e1592ce0ded50d1179227dca1ce228850b3c3fffa706575e7b9c52c0fffa2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Mon, 01 Apr 2024 09:00:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 01 Apr 2024 09:00:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 01 Apr 2024 09:00:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 01 Apr 2024 09:00:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 01 Apr 2024 09:00:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 01 Apr 2024 09:00:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8d6b5fc7c9915bf1b898a9c0700e36ddd3e26002dd338d06fbbca24e9c69c1`  
		Last Modified: Wed, 24 Apr 2024 08:05:22 GMT  
		Size: 199.5 MB (199547401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010a954122a1001c816f08aa9329601a5a088ff9077606ec7283a5d249879ff9`  
		Last Modified: Wed, 24 Apr 2024 08:05:10 GMT  
		Size: 9.5 MB (9479971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7ab86444e18a3e0d545ff72212cc4fb6045decbd473e6e4e788e2a1f7a46ba`  
		Last Modified: Wed, 24 Apr 2024 08:05:09 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841862551602577393d863231667e4a1574d572f6af08114e61fce882607b59d`  
		Last Modified: Wed, 24 Apr 2024 08:05:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b001674369082c2ec3547c8e0a4d6ef994590b117c4bdc30277cfabc1d8c6482`  
		Last Modified: Wed, 24 Apr 2024 08:05:09 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-11-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3835eb850cb8172a736d55bcaa27f13da489c46901a4545da420f95831e61f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235021188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c157664271c0fada46846121feb6fb99cd2de0900b2640ce22ad98df19b4661`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Mon, 01 Apr 2024 09:00:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 01 Apr 2024 09:00:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 01 Apr 2024 09:00:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 01 Apr 2024 09:00:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 01 Apr 2024 09:00:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 01 Apr 2024 09:00:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1396d49ff226d2a493b772a35f12bb4e4f822530a399fe4605c692807af1943`  
		Last Modified: Wed, 24 Apr 2024 08:29:07 GMT  
		Size: 196.4 MB (196359927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8e2d44ca1c2ab696754da5ee812cff04620310a5718bc2be3fd017bcf3dd44`  
		Last Modified: Wed, 24 Apr 2024 08:28:57 GMT  
		Size: 9.5 MB (9479941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7807402d4681a4d697e2d56dfb3761491edbdb7a43c25b7da97c089ae8d9703f`  
		Last Modified: Wed, 24 Apr 2024 08:28:56 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a62c92cf7cc34799251e3f3e8392248b0ddbd0c4231803b64ee63513a18e96b`  
		Last Modified: Wed, 24 Apr 2024 08:28:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9df68e8a5cbf080ad0c1b44aa82415b0c178c43726facadab7c7015470a2fdb`  
		Last Modified: Wed, 24 Apr 2024 08:28:56 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
