## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:568dbc954e4ca5082323706d4cac5260729e4cd369b23aa4bfff5305cb4852ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:96696920034936174834dd0569779d3e6b43c47280dd694cba32901a02d54572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297812042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f781c66f165e52a6fe392bbc68d4141385ae18786e841030757410c181d771`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaafacd94de0ab9becdc9ead4b8a4e91208459bb59410b41d5a3f2357ad4fd1`  
		Last Modified: Thu, 28 Mar 2024 06:52:35 GMT  
		Size: 143.7 MB (143720392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58960c18b0644d73b7240ad722457b2472b6e7548fc23a1f8f82e663d94f4bc`  
		Last Modified: Thu, 28 Mar 2024 06:52:31 GMT  
		Size: 3.9 KB (3872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeb7cca01973b0f1fa6ff6ca3503bb5edf2c33f4ef496103918dcc935647fe3`  
		Last Modified: Thu, 28 Mar 2024 06:52:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc7263d004348d66226b619476440362171d34d3723b6c413a6a88bf8822b3`  
		Last Modified: Thu, 28 Mar 2024 06:52:35 GMT  
		Size: 124.0 MB (124007091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3159fa63e887ab79b5dc72a3a014ccee96212c953c6238416c90f216203a5410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0a42274117cc35e221cc128bb0150ccf738cd4555178eb70bf103a96221afc`

```dockerfile
```

-	Layers:
	-	`sha256:6b2790142d65744d17dbe30822d49b0c2677eadea6efab6727d226bfdc624f65`  
		Last Modified: Thu, 28 Mar 2024 06:52:32 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdaebfc8b12a89cd6a014fd78558c8a7308a101352fda64509094fbc27deb617`  
		Last Modified: Thu, 28 Mar 2024 06:52:31 GMT  
		Size: 22.1 KB (22061 bytes)  
		MIME: application/vnd.in-toto+json
