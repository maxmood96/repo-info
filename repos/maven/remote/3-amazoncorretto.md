## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:ead689ca05365bf7531277926b44f58eee0e0da7b4f586cc3f5208114aac5db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:7087c746135a173487bc2b9a1975194d30c3972ad01c315ad0912e662b698a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.4 MB (371399088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e486925bbacc5750fbffdd79b1dbecf52cd77a3444d0109ef24209406f7912`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Mar 2024 23:50:32 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Mon, 11 Mar 2024 23:50:33 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 02:48:45 GMT
ARG version=11.0.22.7-1
# Sat, 16 Mar 2024 02:49:12 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 02:49:12 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 02:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6421de20b13ff010a684d7e8e5c27f921df3c98c329837d597ec3fbda5ab9493`  
		Last Modified: Sat, 16 Mar 2024 03:06:21 GMT  
		Size: 147.9 MB (147879049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a310fbe5373150e7cd5359a3b7c649a83044e4a6a93ce53033a077c519f5915`  
		Last Modified: Sat, 16 Mar 2024 11:12:30 GMT  
		Size: 151.4 MB (151388157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6565f0a450dd2dd013576e74fda3c6335e5eb91994543885cc30dfb58d295e`  
		Last Modified: Sat, 16 Mar 2024 11:12:18 GMT  
		Size: 9.5 MB (9479946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97c9c601ab3142e7f068f1f8f73ac0bf641f71e6199e12be0b34bfd89732710`  
		Last Modified: Sat, 16 Mar 2024 11:12:17 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75912317bf7d95818bd1887bcf2654cc22e11180abd9e9271c9d8a4a7476a3ab`  
		Last Modified: Sat, 16 Mar 2024 11:12:17 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377605b11705abd501f87f937b75ff25f9dfad3065bcc8bcf8bd4402dae3174f`  
		Last Modified: Sat, 16 Mar 2024 11:12:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:76e2bf343bae2b934404df17941cd131f827cc8e636f8aefaa457348447f8ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.5 MB (341472789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce259a88f3810caa671da89699ba9202d6772036a13ed272dd6e19c07b7a939`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:58 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Mon, 11 Mar 2024 22:39:59 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:11:45 GMT
ARG version=11.0.22.7-1
# Mon, 11 Mar 2024 23:12:05 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 11 Mar 2024 23:12:07 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f6b91a2f6b8e4be4797bf4e8deb57335399979d51d5765b1eb8e8158dd4226`  
		Last Modified: Mon, 11 Mar 2024 23:21:54 GMT  
		Size: 145.1 MB (145059293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0541df06268a20b4d3ed417d916f7cbed581f4a3a7270d378fcac6eee95cbc`  
		Last Modified: Tue, 12 Mar 2024 00:19:25 GMT  
		Size: 122.4 MB (122355808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be762803a5a58d6700f2954360adef2199de23a9479aac4df3d8ca8e823e458`  
		Last Modified: Tue, 12 Mar 2024 00:19:17 GMT  
		Size: 9.5 MB (9479932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c632a335021da2b2f714e88d0b12e1f644ca4dc92788f52d51c4a5726bb95774`  
		Last Modified: Tue, 12 Mar 2024 00:19:16 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff10a31997646e9e4441570c0aca167dd9feff16067e9d76cb8a6385d474554`  
		Last Modified: Tue, 12 Mar 2024 00:19:16 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddef31d4f0fc463fb143fdf98544d7936a0b8f7e0ce479f6c86cc4835e35c7f2`  
		Last Modified: Tue, 12 Mar 2024 00:19:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
