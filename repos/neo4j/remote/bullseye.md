## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:b0a16677c899cf0896d75191af8099b016a6ea4e27707f699aa7883ccd38e027
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:fe9d25b8442a58e4578c3f9f9ea1625d3d2f009ac8a48f980e1396f798340b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422688883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514c109cc8146de994e21af1014fcce1ffb0806df29f7ddce122d31c8e685eaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Jun 2025 13:23:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 19 Jun 2025 13:23:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Jun 2025 13:23:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7be4a4e8f374c66df880abd6a236ff789cb61c1b22746b17cfad343abc3e5505 NEO4J_TARBALL=neo4j-community-2025.05.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 19 Jun 2025 13:23:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Jun 2025 13:23:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 19 Jun 2025 13:23:43 GMT
VOLUME [/data /logs]
# Thu, 19 Jun 2025 13:23:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 19 Jun 2025 13:23:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 19 Jun 2025 13:23:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2ad26a708c4cdd4f5fa39b0e5094533674d07701c3b03e8619af709f11f583`  
		Last Modified: Tue, 01 Jul 2025 05:44:49 GMT  
		Size: 157.6 MB (157634504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767fd88a85ac5f27df99c5c46f3701c63c5fe41dfe24a9707c0a27c1be2877c6`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0064a635d7d0e25f470c544fba7a189a4a9e835b4051d3c9b9a3426feaffb37a`  
		Last Modified: Tue, 01 Jul 2025 02:27:53 GMT  
		Size: 10.0 KB (9979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbe0a1847a66ba3a7ce64a05ae4247308cced9a3c0090775c5db17ca789664b`  
		Last Modified: Tue, 01 Jul 2025 05:44:57 GMT  
		Size: 234.8 MB (234784482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:56bff76b51f9f0b60c31ccc47507324a9bbf26ce616c1fbdfe35a04096dadc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4626096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d324db742045fd1a93f3da9c0f1d8251befa3de9ffd1c79731a81da31c3fad7b`

```dockerfile
```

-	Layers:
	-	`sha256:8e4d2abdd0dc822d42cae1d023aed80aa0e372bcb6480a5ce5a2eefe606adf66`  
		Last Modified: Tue, 01 Jul 2025 05:43:19 GMT  
		Size: 4.6 MB (4601990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a800b4e6f4e0be12276fc7b9ff4617afe5f1293de8697d754ba7b7048445ff`  
		Last Modified: Tue, 01 Jul 2025 05:43:19 GMT  
		Size: 24.1 KB (24106 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db870aba6b3f3c7fa7281c88a43e570047dea230a425a1ffb8ec77d28e699707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.7 MB (418715808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43455d72d80557fac81982470350e6460a74ad14e36984df5348932ce3d4647b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 19 Jun 2025 13:23:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Jun 2025 13:23:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7be4a4e8f374c66df880abd6a236ff789cb61c1b22746b17cfad343abc3e5505 NEO4J_TARBALL=neo4j-community-2025.05.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 19 Jun 2025 13:23:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.05.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Jun 2025 13:23:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 19 Jun 2025 13:23:43 GMT
VOLUME [/data /logs]
# Thu, 19 Jun 2025 13:23:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 19 Jun 2025 13:23:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 19 Jun 2025 13:23:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a05b7675310ac1706c242efff47ecbf4b89d0e0e2b0670389c8f811b1f50b5e`  
		Last Modified: Fri, 20 Jun 2025 20:48:50 GMT  
		Size: 155.9 MB (155928824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefa24f91a81bdf8931c39e7f2173f5050500c5aa7131e069ea4c1f0782d6b3f`  
		Last Modified: Fri, 20 Jun 2025 18:33:43 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f67f787c8e7a93866c09485eead84009150fcedecab7d03b0bf178a133e516`  
		Last Modified: Fri, 20 Jun 2025 18:33:43 GMT  
		Size: 10.0 KB (9980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274c8fe8fc68ebc3966fdce0eb42cafefe2e453ace2ceb263bb0ee9848c9e127`  
		Last Modified: Fri, 20 Jun 2025 20:45:00 GMT  
		Size: 234.0 MB (234028920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:25788b3ff633428b63b0b3300fc60d2fe8a4d22769577ddbadbbd7161fe952c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4600310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e936249ea170f89cb863a3d7d8acd0aaf0b15c9e6f4ecf828e24b1bfb55aaa`

```dockerfile
```

-	Layers:
	-	`sha256:4f2a57fb490238e2b67f624b2136d8102fea475d7c3eb22c8c3573da4a882db2`  
		Last Modified: Fri, 20 Jun 2025 20:43:27 GMT  
		Size: 4.6 MB (4575915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c2d95abc3a50acd4c91bf95927e8205ffd6efd7da41fb7f9344726f2335141f`  
		Last Modified: Fri, 20 Jun 2025 20:43:28 GMT  
		Size: 24.4 KB (24395 bytes)  
		MIME: application/vnd.in-toto+json
