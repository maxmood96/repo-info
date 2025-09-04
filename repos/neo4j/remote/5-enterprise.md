## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:85e17928a717ed99d40bfcc740ea885491a25e3b304b67aa4c6a0ab5d6b236d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0db56f721a389da4d35bfd6728eef8df5221e3fd36066bc38cf6cf3c4a705d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650195273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfa1fe5750ed7cae27eaad4396e520626c5d0a84064a26f560369150b8d24f1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Thu, 04 Sep 2025 06:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Sep 2025 06:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=15a484a00722e15893250d9a071190cd97309cefb7c85bcb3a2e69d3764fa447 NEO4J_TARBALL=neo4j-enterprise-5.26.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 04 Sep 2025 06:40:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Sep 2025 06:40:51 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Sep 2025 06:40:51 GMT
VOLUME [/data /logs]
# Thu, 04 Sep 2025 06:40:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Sep 2025 06:40:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 06:40:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b210b89ec360491e1e15bbfeff39823e5cd4ce1de13d74ad2671af978e37b18`  
		Last Modified: Thu, 04 Sep 2025 17:45:25 GMT  
		Size: 144.7 MB (144693284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3566de6717680bba34747188ca0828bb34a781e4d0d09663955b207cb7d74fa8`  
		Last Modified: Thu, 04 Sep 2025 16:48:26 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f84e5297efef8e5c9f992c36f549ab1d81995d2f292a9d7e047c7c2161b099`  
		Last Modified: Thu, 04 Sep 2025 16:48:28 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3531ac986bc6ecaaf4a054f18ab4a27699c33548d5af78141a0566351c6a6814`  
		Last Modified: Thu, 04 Sep 2025 17:45:35 GMT  
		Size: 475.2 MB (475231937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ffe0a6a84cd86d6384a192cf6efc109459882ebef788e928d8a6234dbbc83748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4875982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0101581022708c6e097e34cce61ac113a879715390acd4a7d31ee495536575b9`

```dockerfile
```

-	Layers:
	-	`sha256:b8787d02a55132a96dda22a852f7d6440ff0e65cf0b4e65ba54024a78717300a`  
		Last Modified: Thu, 04 Sep 2025 17:43:54 GMT  
		Size: 4.9 MB (4854954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fcce209d1b6dd5c72431ed928e99fea211a569882a2a06ddd7f978c4abd73eb`  
		Last Modified: Thu, 04 Sep 2025 17:43:55 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3cdd7ff39622e31d01ea9e92def427b5aa2d50d9d76f28b9560474d79fdf35da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.8 MB (646782683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b128ceaa4d9e26220b61e717b8643fdfe736e1d40b5d85f6211eceab27e6dcb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Thu, 04 Sep 2025 06:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Sep 2025 06:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=15a484a00722e15893250d9a071190cd97309cefb7c85bcb3a2e69d3764fa447 NEO4J_TARBALL=neo4j-enterprise-5.26.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 04 Sep 2025 06:40:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.12-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Sep 2025 06:40:51 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Sep 2025 06:40:51 GMT
VOLUME [/data /logs]
# Thu, 04 Sep 2025 06:40:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Sep 2025 06:40:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 06:40:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e2026aa583480d70d13af9d7d6e721f73d5e7e28ff9c70fa6900ceb26667d1`  
		Last Modified: Tue, 02 Sep 2025 05:44:58 GMT  
		Size: 143.5 MB (143542156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a369606cf6c6ebad84e1aa3ffa52e3cad93be5425a2cbd75677eb17f6287bdd9`  
		Last Modified: Thu, 04 Sep 2025 16:50:46 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803595b3dd41fe1e92c04f30183447cdf2e80035a1f8cd76852b643febebb47`  
		Last Modified: Thu, 04 Sep 2025 16:50:46 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f99a711857e5290030762ac6dfd5661a72c0e16a3a570e17acbda3da6d729b`  
		Last Modified: Thu, 04 Sep 2025 18:07:46 GMT  
		Size: 474.5 MB (474476077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fdb5f6a896032576af85c0f02d96208d4816d59a4d52557af8f106c308520838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4849956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c829eaf32c35672e53560a18057bc44d8d81245c42aeed72ab21ec65fb8ac7ad`

```dockerfile
```

-	Layers:
	-	`sha256:585ec2775cf8130b0ffdf707b6af6d08a6358c1df73dacbfb6d9d7cb517139fe`  
		Last Modified: Thu, 04 Sep 2025 17:44:00 GMT  
		Size: 4.8 MB (4828759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0575a907c7951399423b765cb741d7d6bb4ea70582abeb3f39756207dfab6908`  
		Last Modified: Thu, 04 Sep 2025 17:44:01 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json
