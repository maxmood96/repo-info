## `neo4j:2025-enterprise`

```console
$ docker pull neo4j@sha256:8100aa35ac1099825165f5c11439a0e1a18edcf7553426c0e57330d2846231af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:2c249b79f9a57f32a137d0970bbde60d64ff72aceba390879b787d8279ac95eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.3 MB (518327925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bd3acbec91b878aa21b0d2a51b463f247c0701577373f24c83bf9a3fba3e3c`
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3503d987633daf128f2b2da2e510f792c486b221af9fd9ee901e2502afda90e7`  
		Last Modified: Tue, 03 Jun 2025 13:39:56 GMT  
		Size: 157.6 MB (157634456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7243c87fd3d75eb05ef432d6dcc36e51dbb8ee5ecdd1ecab801bfc31f593625`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6b21c33de1f1ed7c6c605f794e88059449440cf3ba58d513668143cff9ffce`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d99cc21091d31a2872a243ba822a3e61240e0329dc166c9e1b7501a26975944`  
		Last Modified: Tue, 03 Jun 2025 13:39:54 GMT  
		Size: 330.4 MB (330423631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5535704434bfa2e75def1a8a2c0557a0594b68250021f0e44967a356511c979f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3611137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f544a10261dd344282ba7c6d6dccf6e9c26ed4f308d6b37b4e6f4e1917c694`

```dockerfile
```

-	Layers:
	-	`sha256:bf665b7307a0592267cf2d42595ed5053c85685e1ce934ede30f59ff54ec9e66`  
		Last Modified: Wed, 04 Jun 2025 00:02:45 GMT  
		Size: 3.6 MB (3589688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96a3f10658fd3dff02508b520d8a96f8d7f0bbe81007fa31d88a9e26261db0b0`  
		Last Modified: Wed, 04 Jun 2025 00:02:45 GMT  
		Size: 21.4 KB (21449 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:47e12bb072e51dca461fd37996beec1ed5fb9ce3553f49286005b337232178d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514283895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d9548c71e99142903458c6fe7754dd1d561b4984ecba201d22e0d38890a23c`
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
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c27f9d6798235ccf5e5f695d350773cf03adc77fea3cfc1049c69b79bf7dba`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8bd0b475f78db8ed20d8d96ea23140014933ba82c5b085543c9079ad898cac`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be540eb6975a8a665ea5731ce2de2924cb935c94c9d0d4da5c156099584824e`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798016306566153e564048468738508e429e0c74184509578200862d6edacc04`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 329.6 MB (329594895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4984ced5a980c3cab245d68091e7e8d01fc30339d5a6225666a72f6ced343d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3611024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d487eb4bbbcbe128699676db0e7cca63e09465c83e9bb3149521c711504376b2`

```dockerfile
```

-	Layers:
	-	`sha256:77ad5bd5ca236d420c2c0fcc9acfdc3b2e677775ba99d906fcc82698ebc853af`  
		Last Modified: Wed, 04 Jun 2025 00:02:58 GMT  
		Size: 3.6 MB (3589382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74da1dab0fd41d03c920954c62752948a754c462329a7afc7db2da0148572c09`  
		Last Modified: Wed, 04 Jun 2025 00:02:57 GMT  
		Size: 21.6 KB (21642 bytes)  
		MIME: application/vnd.in-toto+json
