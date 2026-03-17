## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:e64ca48b5b00ba3e7a5ce05a6366e5cff07af318591d167a74887a153f3f4898
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58acd88f8dd822320d865227e405d620e15b53419f7a002a92ebe056ecf0434a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349152950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfd16da238c0451395d90fda5381eed0af03e3f9387ee4dfc72346802be3e9b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Mar 2026 22:43:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 16 Mar 2026 22:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=06a419691481fe2e08893337ba01fb3486238ff2113202f648aa294c7a5f094e NEO4J_TARBALL=neo4j-community-5.26.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 16 Mar 2026 22:43:42 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
# Mon, 16 Mar 2026 22:43:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 16 Mar 2026 22:43:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 16 Mar 2026 22:44:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 16 Mar 2026 22:44:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:44:03 GMT
WORKDIR /var/lib/neo4j
# Mon, 16 Mar 2026 22:44:03 GMT
VOLUME [/data /logs]
# Mon, 16 Mar 2026 22:44:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 16 Mar 2026 22:44:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:44:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d663f229baac11b023c8965e06f607919b83ad697518b6c543ed99ef1c6727a4`  
		Last Modified: Mon, 16 Mar 2026 22:44:26 GMT  
		Size: 145.6 MB (145628732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd09cd86b61d457bc3f6b7ca6e3e8b0f0dda85c3604def294bc1e1c84a3a1f1`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abe9738acc70b406f7ec0cee5e92178ae547d4a9e04820468e84833243a7c68`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b5e315d69543aab77c1140d1e3f8f34c312d4c7260665418b8f9097c918902`  
		Last Modified: Mon, 16 Mar 2026 22:44:27 GMT  
		Size: 173.3 MB (173252289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:570a24cfae22d6e7293e55fa605d63d01cd928185199e9ba09c137505b1581c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4507735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e78bb7f4fe6561950af2138e8b0e11c37f9f98163fd56c5c7c572ec52fac934`

```dockerfile
```

-	Layers:
	-	`sha256:802512e6901fb4cdf138e88cdea1ca4dc2df4acc7cd4a8977f9f26b9e239df1a`  
		Last Modified: Mon, 16 Mar 2026 22:44:22 GMT  
		Size: 4.5 MB (4486783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dd77e1ee4c9e30e2905424a66d8fa099586279bbd782aa77c10d70c50055b8e`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 21.0 KB (20952 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b4757d1101053face040c4778eb2abb524313b54dc5e2a436d9ac95283ae122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345693595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1685842b1f139c82a95f675b7aeb1b1c9044afe853a78fa8fde2cea68779e8eb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:45:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 16 Mar 2026 22:45:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 16 Mar 2026 22:45:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=06a419691481fe2e08893337ba01fb3486238ff2113202f648aa294c7a5f094e NEO4J_TARBALL=neo4j-community-5.26.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 16 Mar 2026 22:45:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
# Mon, 16 Mar 2026 22:45:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 16 Mar 2026 22:45:39 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 16 Mar 2026 22:45:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.22-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 16 Mar 2026 22:45:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:45:57 GMT
WORKDIR /var/lib/neo4j
# Mon, 16 Mar 2026 22:45:57 GMT
VOLUME [/data /logs]
# Mon, 16 Mar 2026 22:45:57 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 16 Mar 2026 22:45:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:45:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa1c6927d26fd9196e2ee2a08202db79bf6b3e02ee2a67f6b142769ea3f4e21`  
		Last Modified: Mon, 16 Mar 2026 22:46:20 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbe5124f5a7602a67ffe13d102b4bbd8db3f2742e865d168d99d4065502bcb6`  
		Last Modified: Mon, 16 Mar 2026 22:46:16 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7682c37dcc32e519022c262c3cab594249d5ea14c02859eb57d661468b3b8a1`  
		Last Modified: Mon, 16 Mar 2026 22:46:15 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77c696fe48ca7dfb10f1ab5bb2cb1ac9edbf379f1706e005e1abc2bdcab7970`  
		Last Modified: Mon, 16 Mar 2026 22:46:21 GMT  
		Size: 172.5 MB (172498737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:fae3826b71d1c37785c041bdbf86b1f02a929aea024b21f67cac45ccbd7acc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9c5d4c42f692706ffea74cc7bae077b4df633af3fd620aa033a1829f365253`

```dockerfile
```

-	Layers:
	-	`sha256:6ecfeef4cbea331397323ce935eb2ae917cf1a7a3eaed0c5ecbe1a740f5ffdb9`  
		Last Modified: Mon, 16 Mar 2026 22:46:16 GMT  
		Size: 4.5 MB (4460588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3bf3e5faa428bca8ef5bf02c66711094dc775e85a1a0ea3063d415f69b3733f`  
		Last Modified: Mon, 16 Mar 2026 22:46:16 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json
