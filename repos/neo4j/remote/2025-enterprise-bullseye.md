## `neo4j:2025-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:e2bcceb3d5bb8256f985d5d6b77c48bd76bc431bf06cefac83419ab6bff6e78c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:35498e3becbac0337142a50fbbac7dee234037be7f25a53489cda4c7abb049e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.4 MB (534362255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a373a5c5d02edf1a102e68e5f5f6a1c22631f63a490507fab199496f041adc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 10:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=20c1d8a43608aa943885c80d2b496b25aa51126f605a0c0e5b8399424da6aff4 NEO4J_TARBALL=neo4j-enterprise-2025.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Jun 2025 10:48:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:48:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Jun 2025 10:48:21 GMT
VOLUME [/data /logs]
# Tue, 03 Jun 2025 10:48:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Jun 2025 10:48:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:48:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923d95b2c124731966fe418c19ba465a3e6ccaa20e7953ddb1387a8ce71e445c`  
		Last Modified: Wed, 04 Jun 2025 20:45:37 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0b1f090e73674378147f2811aed73ae525610778bbc0e26e1d5f41be651648`  
		Last Modified: Wed, 04 Jun 2025 18:37:15 GMT  
		Size: 3.9 KB (3852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebbee600d35df3c980b2e017844e2751c8d319321d483c2886b56f1b53e7a26`  
		Last Modified: Wed, 04 Jun 2025 18:37:14 GMT  
		Size: 10.0 KB (9980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b5c366e1b5e7d231446fdfaaa464254e71b1b703e3cd8bee617cf15e3a477d`  
		Last Modified: Wed, 04 Jun 2025 20:45:19 GMT  
		Size: 346.5 MB (346457948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4a345830307a968bee29837232b185be4840085e4f47bc1d69f0b39b2c69254e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3d14dd4af0dc512bdc8b1618620900ba2e619d451114b3e368ae3d650e8cfd`

```dockerfile
```

-	Layers:
	-	`sha256:9f8c33918c470f40aaececad3bb9d4f31c02853479582744053b036ba21095ea`  
		Last Modified: Wed, 04 Jun 2025 20:43:30 GMT  
		Size: 4.7 MB (4745838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7609f2269c31e1458d76b4b7e463ec8dc7aede6f5e9628185be19423041bb2c8`  
		Last Modified: Wed, 04 Jun 2025 20:43:31 GMT  
		Size: 21.7 KB (21700 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d490d6bcbb86120cf4ac130f5815976307e6f13205fb8318e36952112f6b8b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.6 MB (529608101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0bb258839d5094b366cdf459d7d871d11a6551f033358b08fcc215b9e4fa92`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 10:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=20c1d8a43608aa943885c80d2b496b25aa51126f605a0c0e5b8399424da6aff4 NEO4J_TARBALL=neo4j-enterprise-2025.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Jun 2025 10:48:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:48:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Jun 2025 10:48:21 GMT
VOLUME [/data /logs]
# Tue, 03 Jun 2025 10:48:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Jun 2025 10:48:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:48:21 GMT
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
	-	`sha256:c0b24deff976ad7df1743e5804c182d64ef0e67027e0be5849233b320bec9fba`  
		Last Modified: Wed, 04 Jun 2025 21:31:40 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55236e9107c59ee2cb850c09fe2499785db89dc3d0c91b5c5d4176a0d7d8684`  
		Last Modified: Wed, 04 Jun 2025 21:31:40 GMT  
		Size: 10.0 KB (9978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e81f369481c65a470aceec4d928c3efae776285b61c77e6a026b42adfed8f1`  
		Last Modified: Thu, 05 Jun 2025 00:02:54 GMT  
		Size: 344.9 MB (344919150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3f2f9433c5ca82ce6b891dd63c6c82490028e72786f0c477034e7ff2861bb135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4741561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9872b8a5fe61d41da117de49954f7d789134a67a9af91088e62438eeaeea476`

```dockerfile
```

-	Layers:
	-	`sha256:45cfef64ee4414b57ea8b6053348abb7d0c7cb99a17c51bb0881dfaf6a12f2d2`  
		Last Modified: Wed, 04 Jun 2025 23:43:33 GMT  
		Size: 4.7 MB (4719667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c4d526f2ed1a3971f3fe7c1c90b1299d22053c290e4cd877aad3d6848153351`  
		Last Modified: Wed, 04 Jun 2025 23:43:34 GMT  
		Size: 21.9 KB (21894 bytes)  
		MIME: application/vnd.in-toto+json
