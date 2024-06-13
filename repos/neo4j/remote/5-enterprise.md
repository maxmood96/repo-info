## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json
