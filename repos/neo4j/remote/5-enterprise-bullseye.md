## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:8e21b7ec62576e09a66270f5ec9d1257bc4f71ce101ef7cc825a517b23f0f5d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:590c27d5bba2d730565a557a7814fa882a9f15e04c1764cb201eabab9e604eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 MB (594431321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f72a2667dc06e9e63841b1c356d91f347e325e651cc781bcdd02fc41feed89`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 12:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 12:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c1b51e08cfb5d8063240656ab58ee0766264b63b27cbcdcff2d28e77f8972534 NEO4J_TARBALL=neo4j-enterprise-5.24.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 12:51:09 GMT
WORKDIR /var/lib/neo4j
# Thu, 03 Oct 2024 12:51:09 GMT
VOLUME [/data /logs]
# Thu, 03 Oct 2024 12:51:09 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 03 Oct 2024 12:51:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 03 Oct 2024 12:51:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de4795283092d21e11e6420af407ae339d038ee0f6e57eff13590d16716114c`  
		Last Modified: Sat, 12 Oct 2024 00:55:41 GMT  
		Size: 145.2 MB (145166553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ab5b8006fd2866d0d47f203198ffcf9b3488722d70bbb98d0cdeff72448bbf`  
		Last Modified: Sat, 12 Oct 2024 00:55:27 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e53848ab5f1a212ed1451e202eb7325a4265c9b6aaac6d17b7199b032740`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b411f01df6bc07ae62e8f24d3ca78ff67f63d59140b4c506941d4ee04f045b`  
		Last Modified: Sat, 12 Oct 2024 00:55:44 GMT  
		Size: 417.8 MB (417822283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f183703ddeef3cd31de960d02e0d63ebfb6a09c288771ac5ff7d3dcaa4303d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3488994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbfe855c2d8e2c85eb0f650e6be7e05309957de9c404fac9c7935fc96237ef2`

```dockerfile
```

-	Layers:
	-	`sha256:c7841d8712194410176ae5e538da763bce05265594ba1741489a587ae6b2841a`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 3.5 MB (3467938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dbdf2a9fb713de81bdfd1ceb95b57146364555e4dbda32e86b05fb613ca526f`  
		Last Modified: Sat, 12 Oct 2024 00:55:39 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ec19c1c6fe9669d898aadc752384d42628f22fa917f3e14ca74ed4b3332fc821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591864096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e000483c947a1e8db7102bd51a47c62b4736d961a4ab20b789830d460e9e623`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Tue, 15 Oct 2024 14:23:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Oct 2024 14:23:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7ce97bd9a4348af14df442f00b3dc5085b5983d6f03da643744838c7a1bc8ba7 NEO4J_TARBALL=neo4j-enterprise-5.24.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec42ce9ffa92f804e17aa8adf95872a1a3574976006d0237f2997f04f1c8c81`  
		Last Modified: Wed, 16 Oct 2024 02:23:59 GMT  
		Size: 144.0 MB (143959469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd8bccfa2c272430e3fba877e5134fc0f293a75aceed8d1c029b038423850c6`  
		Last Modified: Wed, 16 Oct 2024 03:49:37 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa598d839e692638b128738f4c2219fcb712bfd9c215f3087893a2c831d11c0`  
		Last Modified: Wed, 16 Oct 2024 03:49:37 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2422a7f4e577740151e646ed9fd5db9ee63bf230f85da7454b1ededdac8c0d`  
		Last Modified: Wed, 16 Oct 2024 03:49:51 GMT  
		Size: 417.8 MB (417815564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:53a596f31bdc50af326c749a3576be6fbbfd3525cbc01005d61946f8c72f556f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0490315cb6305f049d98e305cfedd77564aafb9e29ce3ca347e62025de99df22`

```dockerfile
```

-	Layers:
	-	`sha256:61eb6de48181a61fd8030d07306b4d39f19a810a7319868316293fd72d74b1e0`  
		Last Modified: Wed, 16 Oct 2024 03:49:38 GMT  
		Size: 3.5 MB (3468879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bcea737928af6c55a4e0becca095ab38996cb66c8445878a6c96337391670ed`  
		Last Modified: Wed, 16 Oct 2024 03:49:37 GMT  
		Size: 21.2 KB (21236 bytes)  
		MIME: application/vnd.in-toto+json
