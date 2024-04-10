## `maven:3-amazoncorretto-17-debian-bookworm`

```console
$ docker pull maven@sha256:8c6891e66ca991ba2caf6d5b725b622b4f8816b358347f896f0f638c6b8d1d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:15de809aac0149281c06673f2acf750d6dfa5bd38019071910220d052e9e74ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236400087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d5afddf69dd4fe422337a86502637e793b6a75866ab5ac42dbc75d73cb237b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Mon, 01 Apr 2024 09:00:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef56c6d1b11942e0df0bb9545b99c0938494dd07a10bce594a7872b6e2a6a75`  
		Last Modified: Wed, 03 Apr 2024 00:28:10 GMT  
		Size: 197.8 MB (197794589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89cd1b4b14a3227f64b3ff576b88836cf588e0ad098685c5828176bb2be4cea`  
		Last Modified: Wed, 03 Apr 2024 00:27:56 GMT  
		Size: 9.5 MB (9479936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d1337b0fa5ffa05d6625be10368f54c8d123bb440b8147ac291ccf11714fe0`  
		Last Modified: Wed, 03 Apr 2024 00:27:56 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0526df711c744a89c8047fd0184b9856ed33335a8a848748a629f59654bef19a`  
		Last Modified: Wed, 03 Apr 2024 00:27:56 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef0f10235367f7be7691dd635deca229911667f112604be9787f03efd9a881`  
		Last Modified: Wed, 03 Apr 2024 00:27:56 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:65d513c1725a7f6325af6258fa52854408fe4d3989c84f653a700543eff3dec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234787591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c918e9f82e7326264910912a9ca018a595ae15c0ce8bbea0bc1e3c9308f5744b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Mon, 01 Apr 2024 09:00:46 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Apr 2024 09:00:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5661c55a252c4b9de35a89a25ba22bc608199e1a6bf9b15eeebebf7d0048fa`  
		Last Modified: Wed, 10 Apr 2024 05:17:30 GMT  
		Size: 196.1 MB (196144108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa278a51343151e942e98ae4b92d749dced54336adbcd462b312031f37a8d9af`  
		Last Modified: Wed, 10 Apr 2024 05:17:19 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134025ae3530a07f348ca3d8d8114e76971d2b1c12097e26b2ef9091faab083a`  
		Last Modified: Wed, 10 Apr 2024 05:17:19 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b832817286460e3b41132d072516b7d84e64886afb362778b8f9268c1cb9d720`  
		Last Modified: Wed, 10 Apr 2024 05:17:19 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bfd1bf8a96f4b6957a94746a80729e57f06c2d3cf433797284ff5af3355058`  
		Last Modified: Wed, 10 Apr 2024 05:17:19 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
