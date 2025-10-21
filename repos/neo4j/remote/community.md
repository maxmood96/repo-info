## `neo4j:community`

```console
$ docker pull neo4j@sha256:914a42cf848b4dd9d0daaf0f402c3a0ebc41f8a6eebb8e5f3e567cac007adb92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:eae5b0ec9e4cadd46636b94f7dbdcf4336f6ee237590a7676119ac6561b7eea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399302038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7176b421c41b439188045b84a233aeb532b5f65c7cddb2e3c3ab103ffd1bb07e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Tue, 30 Sep 2025 13:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Sep 2025 13:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=997928463c687a96433720610c3091969fd4d5f76f8a12d09a6149bddf65927a NEO4J_TARBALL=neo4j-community-2025.09.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4d3ed4f508f7ba0867209fa0b04d6a613cbdb756706d42e0256514184c0ec4`  
		Last Modified: Fri, 10 Oct 2025 05:45:49 GMT  
		Size: 157.8 MB (157804768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa20373901d90ee8a871ddac7654ccadadc414c55648a7b5e7848a4264dee3b5`  
		Last Modified: Thu, 09 Oct 2025 23:00:32 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e259da529216f5a027a8c5dad5efbda75bf188bad25bdaa77e5569e58aa57cc3`  
		Last Modified: Thu, 09 Oct 2025 23:00:31 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa9c2c55d9052326c036c7273679bd3be0ca2e58e9cdf1f46422729711354b6`  
		Last Modified: Fri, 10 Oct 2025 05:45:48 GMT  
		Size: 211.2 MB (211225016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:cf64e95c8b36132670fa748ca9c3b7cd7b7f58a67a37cfddf8c1508fb2c7cedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4629402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6db4faabc0ba44d66e44033309219ce05ebdaea11ede00afc4cef6d3a4cd3b`

```dockerfile
```

-	Layers:
	-	`sha256:9e97f441f05067b429702fdba24d1a03418f6359c014a677d6e7c3d96a3f00ae`  
		Last Modified: Fri, 10 Oct 2025 05:43:21 GMT  
		Size: 4.6 MB (4605294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1faaab35eaab3a57e69b4660eb50aa8fb36136d485682dd479285363db78161`  
		Last Modified: Fri, 10 Oct 2025 05:43:21 GMT  
		Size: 24.1 KB (24108 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2f0369a88cb3a846a6578bf73dfea38343f06b59d6f7b96117f762247726c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.3 MB (395313068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3811837fe591b3ad02da152d3157517a408e7dde12cc6279212cac139e960381`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 30 Sep 2025 13:19:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Tue, 30 Sep 2025 13:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Sep 2025 13:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=997928463c687a96433720610c3091969fd4d5f76f8a12d09a6149bddf65927a NEO4J_TARBALL=neo4j-community-2025.09.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c58427f0e485063420619bb5b5890b8de24bc0ca9e1890b5614e50166d3173`  
		Last Modified: Tue, 21 Oct 2025 08:45:48 GMT  
		Size: 156.1 MB (156081199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4b08912389b82d7975ce75b19766993dc3cd0e146d86ef463b4edb51c70db4`  
		Last Modified: Tue, 21 Oct 2025 02:36:43 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8bc76b617287b13f0cc5b5a93edccf0a2eaf64101321c564540359abb60286`  
		Last Modified: Tue, 21 Oct 2025 02:36:41 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ed096c98df9d009543d201eaa8d243544ee08e22851b770e80d13af141b672`  
		Last Modified: Tue, 21 Oct 2025 01:50:50 GMT  
		Size: 210.5 MB (210469553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e908417602590aa200aed1e9e27a6cec09e349b32c37d2b57be691c1a2b904af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4601992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3266276724925ae22308db90c7735c1ec793ac02d795ccaff3aaae944861e7d7`

```dockerfile
```

-	Layers:
	-	`sha256:38f542ce7c63575aa505c82b7a476d5113e55ebfeec4fcc867a00051062ef4f3`  
		Last Modified: Tue, 21 Oct 2025 08:43:20 GMT  
		Size: 4.6 MB (4577595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9aef8bfef7f1d12a24b869d6f706753cfa9a995cd215e4cee5e63afc1fba0b`  
		Last Modified: Tue, 21 Oct 2025 08:43:21 GMT  
		Size: 24.4 KB (24397 bytes)  
		MIME: application/vnd.in-toto+json
