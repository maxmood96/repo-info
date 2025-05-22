## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:8b48279e1759a97d36ecec98c72a5f14c028baa4bf0fdde66518453281be4145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7506c58361a1165689f5a70a85ab5b48d2c24831406d091d4813cf1d6ea5e798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.4 MB (513370055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828eaced53ab74193e7af9af094ad01266e66339ddd06555afa4aab872c7c054`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 29 Apr 2025 10:30:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 29 Apr 2025 10:30:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Apr 2025 10:30:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9842e182359caf70877d7e2136f1d8832cbe5a078c8261715af713dc96a6c601 NEO4J_TARBALL=neo4j-enterprise-2025.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 29 Apr 2025 10:30:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.04.0-unix.tar.gz
# Tue, 29 Apr 2025 10:30:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.04.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.04.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Apr 2025 10:30:01 GMT
WORKDIR /var/lib/neo4j
# Tue, 29 Apr 2025 10:30:01 GMT
VOLUME [/data /logs]
# Tue, 29 Apr 2025 10:30:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 29 Apr 2025 10:30:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 29 Apr 2025 10:30:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a6f4f3f9d0309c6ebaadfc45ead6e1181d8f975a05d6de296e3bd987101b77`  
		Last Modified: Wed, 21 May 2025 23:22:44 GMT  
		Size: 157.6 MB (157634466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1022650f7fc94702c1394462141831770e4553acbf05b5dc2db33e2ce27bcc88`  
		Last Modified: Wed, 21 May 2025 23:22:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ef026818f64103d202eacb905d144ef7d892082ed0ea538a7aaae3e231fda9`  
		Last Modified: Wed, 21 May 2025 23:22:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4638508a4707ec4ab1f5052d421702d589e95510d1a133709c02d7d450bc7f73`  
		Last Modified: Wed, 21 May 2025 23:22:47 GMT  
		Size: 325.5 MB (325465754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fddb51bbf3f14ef63b2eb7483d30846607c5d2635f5383c10470076a3e57cfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14774849f6193e4bea557bfc59cdb2dbdc871fe603b8fba4d4cb21c43f6c3f1a`

```dockerfile
```

-	Layers:
	-	`sha256:999e1cbf216070b2aba2f22725d83e9113a12a445775c3aededa23e6202a4d05`  
		Last Modified: Wed, 21 May 2025 23:22:42 GMT  
		Size: 3.6 MB (3586820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91afb9e86aeec49d24da8fc59fea7d69d9212537e8343fa87c2db12144ce6083`  
		Last Modified: Wed, 21 May 2025 23:22:42 GMT  
		Size: 21.4 KB (21449 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:10b80db9810b632ea430ddae8c1d9d7f4363ce4cd2f2dc4d94c04cb8d11ceb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.1 MB (510115355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b131d15d3ec15fa787b8b65f8d914bf1e3a4ff829f443661880b878a9fd5424`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 29 Apr 2025 10:30:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 29 Apr 2025 10:30:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Apr 2025 10:30:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9842e182359caf70877d7e2136f1d8832cbe5a078c8261715af713dc96a6c601 NEO4J_TARBALL=neo4j-enterprise-2025.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 29 Apr 2025 10:30:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.04.0-unix.tar.gz
# Tue, 29 Apr 2025 10:30:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.04.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.04.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 29 Apr 2025 10:30:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Apr 2025 10:30:01 GMT
WORKDIR /var/lib/neo4j
# Tue, 29 Apr 2025 10:30:01 GMT
VOLUME [/data /logs]
# Tue, 29 Apr 2025 10:30:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 29 Apr 2025 10:30:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 29 Apr 2025 10:30:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6aafe23ee3a98ee826ee0b23fea099b9283485a0939c89bf6b8cac4331d6c`  
		Last Modified: Thu, 22 May 2025 03:12:25 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d3fd6780ce67ed45b09fd8a2401a57894096fb44afc0258ffad7a510b20553`  
		Last Modified: Thu, 22 May 2025 03:13:57 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031131dd7c32aa8ccce5a1173e2362ef00d244720ea0fd6b0022f30cc9fcb329`  
		Last Modified: Thu, 22 May 2025 03:13:57 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e348daeacb428dd70106d244d2f111483c58b9eb59b3f0db1633844ba4bbf8`  
		Last Modified: Thu, 22 May 2025 03:14:05 GMT  
		Size: 325.4 MB (325426349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:07a732942506709b16c181cdc4fdbe526b0cc292864268252c69062888b53bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a329f411e7628edd50b6ca4960e51f6bf894efc73d670e44f044272e4de2c8d8`

```dockerfile
```

-	Layers:
	-	`sha256:d90ebcd9c1e38dd5b7caa9256b77ef9e51a5e6484e64365e22d470f1203e3911`  
		Last Modified: Thu, 22 May 2025 03:13:57 GMT  
		Size: 3.6 MB (3586514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db231901a43196d3052be4ee2da36678da2d9aae8a47042af63af256ec642d96`  
		Last Modified: Thu, 22 May 2025 03:13:57 GMT  
		Size: 21.6 KB (21642 bytes)  
		MIME: application/vnd.in-toto+json
