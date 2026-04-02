## `neo4j:2026-community-bullseye`

```console
$ docker pull neo4j@sha256:b45dc1123ba2d4dac5f505a6df90b12a762d142918fd327d4312f78e2e6a5256
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:384474d26906d6565a82f62912299ecadbdfcfaecebb6b4b4444e0915dae212f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.5 MB (436470994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2a21481c9d7d48fdbccbe3030d52367548337454a5601f88c746767efc9f86`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Wed, 01 Apr 2026 21:09:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 21:09:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 01 Apr 2026 21:09:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 01 Apr 2026 21:09:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
# Wed, 01 Apr 2026 21:09:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 01 Apr 2026 21:09:59 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 01 Apr 2026 21:10:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 01 Apr 2026 21:10:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:10:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 01 Apr 2026 21:10:21 GMT
VOLUME [/data /logs]
# Wed, 01 Apr 2026 21:10:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 01 Apr 2026 21:10:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:10:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa45be17d453566d54585fbbf8786d9a250a47894b5504d16ef3891f9f035ff`  
		Last Modified: Wed, 01 Apr 2026 21:10:48 GMT  
		Size: 157.9 MB (157857050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5838ea319bde7efab4cec817da4ccee6602e7d405c1265d30135afb8c113580a`  
		Last Modified: Wed, 01 Apr 2026 21:10:41 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5bd9032daf9835eec4662a0c703f10b4e30c8938cd6b0a60eb99733aeee5ed`  
		Last Modified: Wed, 01 Apr 2026 21:10:41 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f92f0579daa37e5f678ac67dd54e198112314696e00ebd7e55eda312d3c52c`  
		Last Modified: Wed, 01 Apr 2026 21:10:50 GMT  
		Size: 248.3 MB (248342054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4ec059736f97a594d2d5bb095e0b8404c46b086df652ae2012c30f7f442c8f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4606329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bdad573bbaa042e1a975217e91a9cbc43c7d0e07b65b0c00cf64c3412534ed`

```dockerfile
```

-	Layers:
	-	`sha256:b2d7bcbd3d9d107c8f02927902f1900e6efc1ff8e7ebf82669dd79542f665a07`  
		Last Modified: Wed, 01 Apr 2026 21:10:42 GMT  
		Size: 4.6 MB (4584706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845c7fff4a7fa04add91ca19c7fce032e67e3a9356cb00ed6278e898e60d03b8`  
		Last Modified: Wed, 01 Apr 2026 21:10:41 GMT  
		Size: 21.6 KB (21623 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:621895f0afe25fe8d632bcf8137086494684c57546beb36ff875260846eb2c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.5 MB (432479587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e64400ef1a7d7661b5f4616179f5cc029a2b7e5e615469d3e11378b5522461b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Wed, 01 Apr 2026 21:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 21:10:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 01 Apr 2026 21:10:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=419c5a471a8b6918570da687215d7d3406983a6ae209fd3d96c2de2a90a5dcfb NEO4J_TARBALL=neo4j-community-2026.03.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 01 Apr 2026 21:10:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
# Wed, 01 Apr 2026 21:10:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 01 Apr 2026 21:10:11 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 01 Apr 2026 21:10:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 01 Apr 2026 21:10:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 21:10:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 01 Apr 2026 21:10:31 GMT
VOLUME [/data /logs]
# Wed, 01 Apr 2026 21:10:31 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 01 Apr 2026 21:10:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 21:10:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434db2f91054a1c45b2e0b9b06cb9bc1c3c7b97234841c0e883ff25ee77fdda3`  
		Last Modified: Wed, 01 Apr 2026 21:11:01 GMT  
		Size: 156.1 MB (156133058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad705d9545d490158985fef75b97b51c2befb818a5e0e7f958214d335f6df08d`  
		Last Modified: Wed, 01 Apr 2026 21:10:53 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388520565ba4eb6a77c959df618d5f34e7fce7645a067cb62c7b3fc337222583`  
		Last Modified: Wed, 01 Apr 2026 21:10:53 GMT  
		Size: 10.2 KB (10187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be615324fb0b6e6bd8076643d4adc336ddf328ec69333c79936a27219044e5f`  
		Last Modified: Wed, 01 Apr 2026 21:11:03 GMT  
		Size: 247.6 MB (247587913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:33f4b73039d88a3d9e012b989d86e9334daa136dcec36b2aadcf021e338c44a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc537c15ec266b21388c20e1a4df310eecc755879a65cb65001e9aebecb14c32`

```dockerfile
```

-	Layers:
	-	`sha256:8dfc16c713bf6546771f80a56eb963e6d46fa6200d02d3aa06eb2693cb4ae2df`  
		Last Modified: Wed, 01 Apr 2026 21:10:53 GMT  
		Size: 4.6 MB (4558535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca072e9aafb7235a842136c2f36603376d6fd572942577681bc9a87c15940b56`  
		Last Modified: Wed, 01 Apr 2026 21:10:53 GMT  
		Size: 21.8 KB (21817 bytes)  
		MIME: application/vnd.in-toto+json
