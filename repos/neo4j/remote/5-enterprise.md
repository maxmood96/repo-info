## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:a75b558323363d109641ed1779b05f612e5b7d0464f90642f55a5ba8071b83e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5eae99831d6e11a4740422e915548e4ae8485b0a9cc688490136411e52ca440e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.9 MB (667889819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f164b1f98129a53317fff03f05de8dd9d84d4dc0a597462abd13f54894a0aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 05:21:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:21:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ff006f997021433017e5e768f83f963f8c181531fafbcffebd53b8f6a585bf96 NEO4J_TARBALL=neo4j-enterprise-5.26.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 18 Nov 2025 05:21:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
# Tue, 18 Nov 2025 05:21:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 18 Nov 2025 05:21:13 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 18 Nov 2025 05:21:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 18 Nov 2025 05:21:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:21:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 18 Nov 2025 05:21:38 GMT
VOLUME [/data /logs]
# Tue, 18 Nov 2025 05:21:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 18 Nov 2025 05:21:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:21:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7fe3d1983242adf9765bc16155a1dc9d621b7e54d32060f806fc121a65fd637`  
		Last Modified: Tue, 18 Nov 2025 02:28:43 GMT  
		Size: 30.3 MB (30258483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db90977abc5f25e06151c65260ae9c8ee6cfcf7e5bd028f015c338e825b3694`  
		Last Modified: Tue, 18 Nov 2025 06:46:52 GMT  
		Size: 144.8 MB (144847974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e25c415ca70a90ea9a191b52c91b392c82eede4a10a1f5d9886285e047ec22`  
		Last Modified: Tue, 18 Nov 2025 05:22:23 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9186089ff50057a8bcc6878b0ec68be4e2a1cdeaa147c4198f4a55e9d4859ed`  
		Last Modified: Tue, 18 Nov 2025 05:22:23 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840696b897832612b1319da8ff742400b3589b6188d01d8d8652317e3173be73`  
		Last Modified: Tue, 18 Nov 2025 06:47:02 GMT  
		Size: 492.8 MB (492769422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f9bc13f46b0cb883e9db2ceac14ef80ad283b2bac7841d429072a8eb3cb22469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4864205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adcbc7fa17f64d4181f7fcaf7a623a575c0cd0d7002556f840a55fb27a1ecc7`

```dockerfile
```

-	Layers:
	-	`sha256:53245b0058d88d9444717ea71d69dfefb3b7639c031a3f242e7448867e8b9354`  
		Last Modified: Tue, 18 Nov 2025 06:45:23 GMT  
		Size: 4.8 MB (4843220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3effaa1487665872a7c0d7cbda31053fb353b51e2233d428b64f11bfacbb919f`  
		Last Modified: Tue, 18 Nov 2025 06:45:23 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:448df3f88f3d98f095724b2edbeecf813ac511ff0acd51c0ae70ccd921874191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.5 MB (664456207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000cd11323dbab5132568f52add339654971dbe05da8df657287407c2e2fb697`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:47:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 03:47:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 03:47:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ff006f997021433017e5e768f83f963f8c181531fafbcffebd53b8f6a585bf96 NEO4J_TARBALL=neo4j-enterprise-5.26.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 18 Nov 2025 03:47:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
# Tue, 18 Nov 2025 03:47:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 18 Nov 2025 03:47:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 18 Nov 2025 03:47:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 18 Nov 2025 03:47:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:47:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 18 Nov 2025 03:47:43 GMT
VOLUME [/data /logs]
# Tue, 18 Nov 2025 03:47:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 18 Nov 2025 03:47:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:47:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f96224ae1ca8ef968e29785f18bcaa66c079cdef298be80fdc43182235fd7dcc`  
		Last Modified: Tue, 18 Nov 2025 01:13:42 GMT  
		Size: 28.7 MB (28748465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1bf7cf8499be72efd862c35e030809d2d6c3b13d9de1bdd76c4bb60eba81f9`  
		Last Modified: Tue, 18 Nov 2025 07:06:52 GMT  
		Size: 143.7 MB (143679884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798b01e327a99155a888950a46f67966b249c294ef5e5d6154f850ba4a52a3d4`  
		Last Modified: Tue, 18 Nov 2025 03:48:35 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fa7ac88e93a3678cea5fe92680868a4da91da54d9a10997019313363fcd94f`  
		Last Modified: Tue, 18 Nov 2025 03:48:35 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa87b3ad2089214269fd9095019eb613f869169a059679ab08371735db81068`  
		Last Modified: Tue, 18 Nov 2025 07:06:59 GMT  
		Size: 492.0 MB (492013900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:9f3fad0ff80d962c153c4ee6fc5c6a83e22b15b9e72c67eefcb66b53e27de618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4838179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8778f651bda90e077d59fb9a8a6f6d4cbac86b8c6a03d0775380a0fa12c7434`

```dockerfile
```

-	Layers:
	-	`sha256:ed767057c650d2a1c462bbf037742e1e3c1ae200bad15027430a26a665aa0dbf`  
		Last Modified: Tue, 18 Nov 2025 06:45:28 GMT  
		Size: 4.8 MB (4817025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3832e692a46582c77e39d4fda54a2c7038a6b745ed27fc8b8215e8cafb902bac`  
		Last Modified: Tue, 18 Nov 2025 06:45:29 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json
