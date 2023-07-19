## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:5398ac08d6bd91024c0a2aca150400c7030e7b4fa70e8546fbebb6a7d8d16ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ae47bd9d34974259281c752585035c2d97c04394bec086e203a6465d2c0eb567
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.6 MB (622619473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0921bf17e559e91456e9a3fc95a2206d224d4c4268ce34b1d7b9f0bd0fa9dca8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:58 GMT
ADD file:bd80a4461150784e5f2f5a1faa720cc347ad3e30ee0969adbfad574c316f5aef in / 
# Tue, 04 Jul 2023 01:19:58 GMT
CMD ["bash"]
# Wed, 19 Jul 2023 20:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Jul 2023 20:42:13 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 19 Jul 2023 20:42:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 19 Jul 2023 20:42:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Wed, 19 Jul 2023 20:42:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 19 Jul 2023 20:42:39 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 19 Jul 2023 20:43:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Jul 2023 20:43:11 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jul 2023 20:43:11 GMT
WORKDIR /var/lib/neo4j
# Wed, 19 Jul 2023 20:43:11 GMT
VOLUME [/data /logs]
# Wed, 19 Jul 2023 20:43:11 GMT
EXPOSE 7473 7474 7687
# Wed, 19 Jul 2023 20:43:11 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 19 Jul 2023 20:43:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:faef57eae888cbe4a5613eca6741b5e48d768b83f6088858aee9a5a2834f8151`  
		Last Modified: Tue, 04 Jul 2023 01:25:03 GMT  
		Size: 29.1 MB (29124829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ef95bdc735d909eaee3e2c5c5072bf884101807a69a15402bee83aab9a13f4`  
		Last Modified: Wed, 19 Jul 2023 20:43:50 GMT  
		Size: 192.6 MB (192580400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305a772a1f0398766dad78e8918cd6e2afd4fa62e6af50f678e0b22c12dbeae9`  
		Last Modified: Wed, 19 Jul 2023 20:44:10 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777d13371b09c3cb205758c2b7b606bf0581f800196dedf1340464f2522f8fc4`  
		Last Modified: Wed, 19 Jul 2023 20:44:10 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f1434ff981311c68c5ec9dc6e4994aad81566bd797acddfdadce673aaa4379`  
		Last Modified: Wed, 19 Jul 2023 20:44:27 GMT  
		Size: 400.9 MB (400903735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:84bcc2a1ab91432c88b65af60f48a1c08a5afd5a3bab1f6a0a316a2f8cc26248
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615092733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf83a697c802944e8c21b5e534a7909c085da4bb3855681b3fccbaa7281f6b3c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:39:58 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Wed, 05 Jul 2023 04:25:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 05 Jul 2023 04:25:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Wed, 05 Jul 2023 04:25:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 05 Jul 2023 04:25:29 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Wed, 05 Jul 2023 04:25:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 04:25:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 04:25:46 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Jul 2023 04:25:46 GMT
VOLUME [/data /logs]
# Wed, 05 Jul 2023 04:25:46 GMT
EXPOSE 7473 7474 7687
# Wed, 05 Jul 2023 04:25:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Jul 2023 04:25:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368a44711a84ae8605b1c1f0f04cf29732536ca2ecfae7b5a7b10134f3584ec4`  
		Last Modified: Wed, 05 Jul 2023 03:49:53 GMT  
		Size: 191.4 MB (191387679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b23ece0c31811cc3bbeece3a06ba9ebd17bf983ebd1ec6692f7da92b4075f39`  
		Last Modified: Wed, 05 Jul 2023 04:27:00 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d3cc933c14f01fc8d4f7d7a1cdc8f9bae5e9506bc5cc0c1c3ccb9d0421a59c`  
		Last Modified: Wed, 05 Jul 2023 04:26:59 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b51f804cc085e890228ff65b4838e677a06955b7cca38bc716fde91220672bf`  
		Last Modified: Wed, 05 Jul 2023 04:27:12 GMT  
		Size: 393.6 MB (393628843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
