## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:06431b6cfc6f178375cea02352cecac0182b6af784d5d6218cac4f99b859cb72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:43bd0179fcb0bc0ba5627e5eacc6703bedb5fa6acd473e936d5d00bdf5e361da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381947551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24420e1bd81dd267befa700e075e8e9024e1bbe1067c976a247df613aa2a5715`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=21.0.3.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef5468c58a0b4174503bfa5010bd340e5c763a988b59086b50b190a585a4e7f`  
		Last Modified: Fri, 28 Jun 2024 01:26:00 GMT  
		Size: 165.7 MB (165682231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e22e84be39db33114fc08db962e9d867f273bf1a54da0247dc5d0640e4053`  
		Last Modified: Tue, 02 Jul 2024 09:09:44 GMT  
		Size: 144.5 MB (144455825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039b59ecfc970e407121fdb19e15fa9f9d26168efcbfe21e99ca568bf12d1019`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 9.2 MB (9161813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68415c38f3880f70d03080084156be18ceae051c05928c654fe92974daf5dd23`  
		Last Modified: Tue, 02 Jul 2024 09:09:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672dd5d264b738e14ccb71731d8b6124fdc9850a30dc4f7b24fe5d9cd7bde007`  
		Last Modified: Tue, 02 Jul 2024 09:09:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:ba80aacae64fdeba33fcabbb62f34ba13518a335d4c576785a8a36d148cc8948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5629441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e3cb3e57e7013315777a94204b3f5a33143c5f3057f265604cc4a61b4b4704`

```dockerfile
```

-	Layers:
	-	`sha256:18d0b956a364203118d36818bc38d9a17d08cd885d768f8c0bdcb060c53668cd`  
		Last Modified: Tue, 02 Jul 2024 09:09:41 GMT  
		Size: 5.6 MB (5613291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72761ba49539079c61db330c8c8c096f25c1ccc338c09e443a7a7a2362a05b6b`  
		Last Modified: Tue, 02 Jul 2024 09:09:40 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c41e7248c63fff343e064562f9ba0b99f7a511a98060035fceaba9992960cf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.0 MB (357959749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdceef575638b000b34e203109aaf7b7700373ad3e5f021fd092d2921deaa43`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=21.0.3.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da42e6374082caa54e1c7189b0ec27bbdc8f3cebce37dd533779f5708b3aa6c6`  
		Last Modified: Fri, 28 Jun 2024 01:31:00 GMT  
		Size: 163.7 MB (163740247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368ba08a661ad2f3a99832bb4c4d0fc107cb4771db1a42daec0d9044ca91b1af`  
		Last Modified: Fri, 28 Jun 2024 02:08:22 GMT  
		Size: 120.5 MB (120487883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f0b4750493e3eba66f59da3c165bbcddf4cc3fc9f17d18009acf058bd0b4e0`  
		Last Modified: Fri, 28 Jun 2024 02:08:20 GMT  
		Size: 9.2 MB (9161809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e41906c6093b1f744c6dbd99083e78000512b01e3c84eab6d2a036e50f8a67b`  
		Last Modified: Fri, 28 Jun 2024 02:08:19 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db47b1fc3e59865a355d65c9f858947482ff499ec36d3cf2a13a49f21aef245c`  
		Last Modified: Fri, 28 Jun 2024 02:08:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:6521f2efb2f6c5621f09ec27adfe502ab2cb8003e1101e09874a18c2199ed282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a42d7ec9d18122fd31522d381dbf26561fcf30ba0f662695c10a631222c2b3`

```dockerfile
```

-	Layers:
	-	`sha256:0f1e8b7e897f81ded399c889ef2db754e2820af6fb65bf16c6d326579fa1c8aa`  
		Last Modified: Fri, 28 Jun 2024 02:08:20 GMT  
		Size: 5.6 MB (5611918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1400f3f6ac8d6370b48f4dc1db52a3ca52095ec46b6863b89deccff031fe9a`  
		Last Modified: Fri, 28 Jun 2024 02:08:19 GMT  
		Size: 16.8 KB (16796 bytes)  
		MIME: application/vnd.in-toto+json
