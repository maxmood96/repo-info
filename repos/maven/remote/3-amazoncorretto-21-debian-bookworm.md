## `maven:3-amazoncorretto-21-debian-bookworm`

```console
$ docker pull maven@sha256:a021767733621dc571a210812b3c24238dbd62d0e91c79c464b44d4582c87eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-21-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:d6dd72a97067156590987727c4fb0da903780420ba714510a990c671f3378be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251834747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5422cea03155bbdefb8383847251c92bcb31d705d6848a99e71f91951832438`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:40 GMT
ADD file:a1398394375faab8dd9e1e8d584eea96c750fb57ae4ffd2b14624f1cf263561b in / 
# Wed, 20 Sep 2023 04:55:41 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 08:02:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 Sep 2023 08:02:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
ARG MAVEN_VERSION=3.9.4
# Wed, 20 Sep 2023 08:02:23 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 Sep 2023 08:02:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 Sep 2023 08:02:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 Sep 2023 08:02:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a803e7c4b030119420574a882a52b6431e160fceb7620f61b525d49bc2d58886`  
		Last Modified: Wed, 20 Sep 2023 05:00:22 GMT  
		Size: 29.1 MB (29124705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3251c616ce1d9ad142b4c15a2fddfe81dc30281c74e766b24cd337a4590c1a9b`  
		Last Modified: Thu, 21 Sep 2023 09:47:01 GMT  
		Size: 213.3 MB (213302241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c463dc56e5e1fb90ed6c483be5f05762e1bb0bca79162bd56919a4ecc28b4371`  
		Last Modified: Thu, 21 Sep 2023 09:46:45 GMT  
		Size: 9.4 MB (9406418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec83e2392b37626c2d785192f2078ad8073ada1415b3fad9e81708b9b5dc5d77`  
		Last Modified: Thu, 21 Sep 2023 09:46:44 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f55010c0b8e53ac52d6f8e89c456462dac190c3a80adf7884dd19364d13f23`  
		Last Modified: Thu, 21 Sep 2023 09:46:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e6b2a2341a841be5085bf41a1868c1b4bfdda4150006d917a58c9059a28204`  
		Last Modified: Thu, 21 Sep 2023 09:46:44 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-21-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:26686f58542618c6f3629bed1646acbae8e7c82cd93037deb7f48febab2f065d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249633316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24ba6873e83c2bd24d6d3edc8205e2c6240456b448fe189221d917f67879867`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:13 GMT
ADD file:ec1a6e0aedd76c8fdc8544775f8b553f58950e9435f5cfe919f39374e222cfbb in / 
# Wed, 20 Sep 2023 02:44:14 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 08:02:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && rm -r "$GNUPGHOME"   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 20 Sep 2023 08:02:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 20 Sep 2023 08:02:23 GMT
ARG MAVEN_VERSION=3.9.4
# Wed, 20 Sep 2023 08:02:23 GMT
ARG USER_HOME_DIR=/root
# Wed, 20 Sep 2023 08:02:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 20 Sep 2023 08:02:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 20 Sep 2023 08:02:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e886f0f47ef56fcadb6ecaf2116056bbdb273e0afe07ed034498b198d386c04e`  
		Last Modified: Wed, 20 Sep 2023 02:47:36 GMT  
		Size: 29.2 MB (29157221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ce1b085e8c384fea639c094f092ac16731b4b7dcb5d1c8b5a4ca406e70d21e`  
		Last Modified: Thu, 21 Sep 2023 04:21:06 GMT  
		Size: 211.1 MB (211068251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66134e47d2db81c480fe3a24f0695dc1acf90c8d4f7fef22a1f4b987836c110d`  
		Last Modified: Thu, 21 Sep 2023 04:20:53 GMT  
		Size: 9.4 MB (9406465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c878c4bdd41bbd3bcf62280a9241067b075ee6b96e34d68aba0d156cfa67a22`  
		Last Modified: Thu, 21 Sep 2023 04:20:52 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebcf1f6291c4f3d78eadcc57f41e5d6418588e95d05ec551bf08724f0b9a537`  
		Last Modified: Thu, 21 Sep 2023 04:20:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c930b894072641a136822227a66971060385973be496b9ae85aef9ae9ae4d70`  
		Last Modified: Thu, 21 Sep 2023 04:20:52 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
