## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:6bfb613ad72c84e8055566c3c908235b1218520b8d7a9ead710640419c7b22a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:a53dce5ceab850b12b64d6dfb7c60f0305080edbee3b395ebf01b6eae46102f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383118043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67978afe71269e565c6d5f9d622c16da1d442c4cad17c905246f9aeb6c607c1b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=21.0.4.7-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
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
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e141968a6df4e40ff9a246120dba6a9e279f250efe865ccdb1e999bcb2a4d89`  
		Last Modified: Thu, 25 Jul 2024 21:02:23 GMT  
		Size: 165.8 MB (165803978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9dcb1b6c9f3d069b60f92d872a34e1072e216981c3dc53c9b1357b7ffdce57`  
		Last Modified: Thu, 25 Jul 2024 22:01:00 GMT  
		Size: 145.5 MB (145472045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b38cfc916db2626d02d5dea7a6eab190688b8e44570ce1f8f59cc3a937f96`  
		Last Modified: Thu, 25 Jul 2024 22:00:56 GMT  
		Size: 9.2 MB (9161813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d67e2edf295da41a7ceee7bbd107d49b9e05f4e18942304b4ac47e5fd9f75`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0450f50869147e83b4242939f5c2289b76e5ab2b4781714e4f50a72351d64480`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:3af84130f1c219c44d2c715139e5e5b3a3453fd28f2b9f27d6b8b5eaf94849d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2447cc2787ec10700113aa38aaef779c970d792031ba90f61c6069fac37306bf`

```dockerfile
```

-	Layers:
	-	`sha256:7f469bddb0972a1b103e7b7a137fca5f57f6ff1772eccb93d9a9f8016da08b8e`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 5.6 MB (5642650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f83033d1bfbba568773439ad0015841ab058caf7aed592b26ff74a31759771e5`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 16.3 KB (16283 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:75e909912ad82031a4cced76464ed7654593289a9a2e903698e7ed47579ce120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (358993081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3c59696f0274f8ef4c41397c2a925be191e344389d421d093ccdb0a20e54c0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=21.0.4.7-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
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
	-	`sha256:7ae84cee97a8a17573116f568e78a8d7c8415a733e0ccb92185dd2e22634f9c6`  
		Last Modified: Tue, 23 Jul 2024 13:50:38 GMT  
		Size: 64.6 MB (64572700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed31eaf5ef8b5afd3746e02b40fe8e11323e852f853545c35a8303c020e7f54`  
		Last Modified: Fri, 26 Jul 2024 02:02:03 GMT  
		Size: 163.8 MB (163820006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ee793fc301842a3fbcee609f86679a7326fecb64a0e230ab35fdf4d12c3ae`  
		Last Modified: Fri, 26 Jul 2024 03:04:27 GMT  
		Size: 121.4 MB (121437548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de77c0016ee2e977c716f42a6e3b147221e320870934af6954641a2b98f2118`  
		Last Modified: Fri, 26 Jul 2024 03:04:25 GMT  
		Size: 9.2 MB (9161783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac31928cf20ff95511456db3183a92efe4e616e6b5601b4cc63e3ae4a8723f85`  
		Last Modified: Fri, 26 Jul 2024 03:04:25 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3876dd96ee246a4aa7da138fdfcfbf952de743e5ba19a7763b470baed7aa8e3d`  
		Last Modified: Fri, 26 Jul 2024 03:04:25 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:257b72fafbb6e96dc11827336b846bb32e02e775e63d1560de8a3f05bf5375d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5658285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad6b939f4c43b78bb926f6f073597cca559b7dfa570a802903f6b40b8fffc9a`

```dockerfile
```

-	Layers:
	-	`sha256:e1935ef4ea9cc0f1d134869c9a2de34998d49c14690feb9346e3354a4120a257`  
		Last Modified: Fri, 26 Jul 2024 03:04:25 GMT  
		Size: 5.6 MB (5641277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f877d7268c3ff91c4f6588e913cba79753777d5e63693383411b428a5f5c24c`  
		Last Modified: Fri, 26 Jul 2024 03:04:24 GMT  
		Size: 17.0 KB (17008 bytes)  
		MIME: application/vnd.in-toto+json
