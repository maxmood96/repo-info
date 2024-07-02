## `maven:3-amazoncorretto-11-debian-bookworm`

```console
$ docker pull maven@sha256:cf2925579951335c9623caf854b4029afb260493e16334a76581842c54ceeb12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:e46a959282e474e1a974687b93a692d8b084c86a367a3bb53abf134c514d1b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237833855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a77deb104047fcc0f6c36ff7b3532978b7a0b1bb117b0d82ffd21ceb1b2337`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fc385390ec056740ccd82a89959934dba22f458842a0cb46665be2a27b01ea`  
		Last Modified: Tue, 02 Jul 2024 09:25:29 GMT  
		Size: 199.5 MB (199544733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1e3615e081ad2aabb65788e7c90c949de42052a6529ce6c71d53e2b7bd9ce3`  
		Last Modified: Tue, 02 Jul 2024 09:25:27 GMT  
		Size: 9.2 MB (9161811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0d3262e8119e9b1b928f458ddbef832e8efe567987a76a1d72c1ab9b7abc54`  
		Last Modified: Tue, 02 Jul 2024 09:25:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9429264b957c11f05c6e21fac25ccbbbd12e0347f20fcb51c963ba5bd41a201`  
		Last Modified: Tue, 02 Jul 2024 09:25:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:f1f7e38585cc594adc4e111c8ef246d6c53bcdb0e29e18de9e74a06f0d47be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b20130172f1ac01d5fe35a3b5669446879d6f605c018e595cd954e1e20994c6`

```dockerfile
```

-	Layers:
	-	`sha256:af0b9e7a3df43d6b17f5ab9d7effb9c01d1832c668feef7ee3aa46ee0e61e384`  
		Last Modified: Tue, 02 Jul 2024 09:25:26 GMT  
		Size: 2.7 MB (2696336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84e6c225516c9e1c44e0a8cdb6ca82b126cebd1c69108c38b977c7f21a84c4b4`  
		Last Modified: Tue, 02 Jul 2024 09:25:26 GMT  
		Size: 18.4 KB (18414 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:e6c7bdacab09d9621a3f6023d1663f2683f73256525652e419afc43c356428e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234506010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee506a0a257aec96a5b58eb0f0208204a92e4c209e611589598d04a65260dfd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y curl gnupg   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-11-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661fd4a00ea9d02329744f435577b0df113e8c1009c3fd9677ad17c7cd1cec78`  
		Last Modified: Thu, 27 Jun 2024 19:11:14 GMT  
		Size: 196.2 MB (196163500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bbc47afc5d8d082d178cc90950e7c1fbdb91b7a8f861768a914dd901f300dd`  
		Last Modified: Thu, 27 Jun 2024 19:11:10 GMT  
		Size: 9.2 MB (9161803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed634b61121c2ce6ea9528fc296a7c9c1628893fe0fc94219aee1876c733c89`  
		Last Modified: Thu, 27 Jun 2024 19:11:10 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605782cd02df31ea96b6572d5c34397aa6bdc2719fc4dd072b764e01781cde0b`  
		Last Modified: Thu, 27 Jun 2024 19:11:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:606335cdcaa32010f7b3091c18e5e47a756f49eefa0668192ed8a5155c31bfa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2715686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32fcba931450b010aedec6278a3d75b742e9be36cd6fd08db175778a405fe8b`

```dockerfile
```

-	Layers:
	-	`sha256:72478cc896baba0119d8ed865b15c61fddda04315a15cf5ccb41994ef909071c`  
		Last Modified: Thu, 27 Jun 2024 19:11:10 GMT  
		Size: 2.7 MB (2696588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e599019300d4f6515fb358c4c8734c8a404b2ba3e5c1e144ce629c275abec1c`  
		Last Modified: Thu, 27 Jun 2024 19:11:10 GMT  
		Size: 19.1 KB (19098 bytes)  
		MIME: application/vnd.in-toto+json
