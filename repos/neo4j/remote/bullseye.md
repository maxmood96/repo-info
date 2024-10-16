## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:01a95b4d9d07ca282a87e7e765b49ce2cdb9e0a26a790edb7a87b998eb0f92ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e51f6b6de346e7ce7c2043e7d72c8aa4159fe0508b99dcd232a8d6cbbe82fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307942463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0af06819c0439045595684703b8270dba4535a9d5b9872bd1117b570a1e80a7`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=93986d1085b2e50fa1a569876b1a14e4d44b495b670767c0a12697909e8c6aa9 NEO4J_TARBALL=neo4j-community-5.24.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 03 Oct 2024 12:51:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 03 Oct 2024 12:51:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.1-unix.tar.gz
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
	-	`sha256:cb8c33ab0b19e6b120689b330de0ea3883fa577817aa520f27f2680abf9dfc9f`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 145.2 MB (145166545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56df1aa9b59c0fb050d76164de9b8242b758dc7a8d1cb8ad098335883fe46754`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8081c6922dbb34c6fc888ce354327dfcd80ee21418873a730fa3b8d1f6cd4`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf987abcac55a83e26c467c302f31d6c5609a3b3b6cf950ed514b464dc97c1b9`  
		Last Modified: Sat, 12 Oct 2024 00:55:15 GMT  
		Size: 131.3 MB (131333433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f4203663f12844403e726ee3f559361f3d6b9c2b12c07b96ebce7d6674de6a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e8a2b457c081ca6bf73eb76485357be178f6ab669491db4b0a808125dcdaff`

```dockerfile
```

-	Layers:
	-	`sha256:3e103dc9b82f873cdbea430f92f57cb92ed3d33a24be82c969d6d58be76b6679`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57eb1094dfd24bcff155da7532a42231329ac0a05443963719dd17a8c99655d3`  
		Last Modified: Sat, 12 Oct 2024 00:55:13 GMT  
		Size: 23.4 KB (23425 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4a7e9bcf37260ba9f2bab2762d053493a3da22d72d5b93d1feec66a609bf50cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305377943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34742a1d21550bea99e2ba2003fe0609763bc35a18c2025aa14dd3f4fa8acae`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7e16dc4f2c43bc188a358b47c5fad9d0300f1fb2d5998e65380fe425dd8af6d6 NEO4J_TARBALL=neo4j-community-5.24.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.24.2-unix.tar.gz
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
	-	`sha256:64401e46d0c5a0ab511332fca86b89b314831bdca5c6be152b609f7421099bcd`  
		Last Modified: Wed, 16 Oct 2024 03:48:11 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a7ac71d1dddc9a80d4bf9d76ff37cd3411dac80a1dd1f12646b08164ba984e`  
		Last Modified: Wed, 16 Oct 2024 03:48:11 GMT  
		Size: 10.0 KB (10006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2705adb0926d618842318bac95063cf5a0d3401b0649852f86b4b6e099d7b1b8`  
		Last Modified: Wed, 16 Oct 2024 03:48:14 GMT  
		Size: 131.3 MB (131329406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e2dd70daf02e278cecd4ae91178b3a5ba41959ff138f6f45dd6ebb8dbc15faed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e593a1db599097fd12844ae1f6e75369a0f04f67224cd2666845dc58924394`

```dockerfile
```

-	Layers:
	-	`sha256:5de3c7e0b60d95aaaa07d61df5e76cc85ade9e4e91f1919e5234c641ad7fa702`  
		Last Modified: Wed, 16 Oct 2024 03:48:11 GMT  
		Size: 3.2 MB (3180118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae48d0516bea2a629b9b62023e762d4cdbe564f9a82a0cf4d17811df688a0a4`  
		Last Modified: Wed, 16 Oct 2024 03:48:11 GMT  
		Size: 23.7 KB (23702 bytes)  
		MIME: application/vnd.in-toto+json
