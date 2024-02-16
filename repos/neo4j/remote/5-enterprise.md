## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:da50ebd3be31af8d694260cb65eacdfd43c6832211b0c61a634383c5fd42300c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:89d03f7f188c0a3322516c520bda96290304193fdf9fef9aaa568b018a6d9d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.8 MB (547750018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49e9862515e27f215b5320cc800311d5cbcbf28dd76616e75028e53533334b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaefca57510cfe96cdd0df186801c17b403c578f9122d234b154332ee257ab80`  
		Last Modified: Fri, 16 Feb 2024 02:50:35 GMT  
		Size: 144.9 MB (144892421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa03c9f9804952178187613bc2fa76d74fc6d175f8357ae13532e1b18987806d`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a0ff91c311f1d1f6dfbd3b51e338f77aa0beafd0cd7bf6999a8ccfad0422b9`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b643d252a45a25591e10c99f3af3d29141aadfe0ddb2f910970053bfa24a9092`  
		Last Modified: Fri, 16 Feb 2024 02:50:39 GMT  
		Size: 371.4 MB (371421846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0f7f0c95990f363af6a519635aa6f5e0390a5f8f9e0de95268370f02ae738d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341328f4a06c1dcc5356e890027f22d8ff285f2de7e6b409f7e47b5bd05cf6f8`

```dockerfile
```

-	Layers:
	-	`sha256:2eab2163360ae36baff8fda9e2e22ffa86adf2f9f7e47dd4dfa0baf63036f97a`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 2.8 MB (2757446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9224aef310e85f9464aee8033eff7204f9b91d65fdb410c0f068174830a4332`  
		Last Modified: Fri, 16 Feb 2024 02:50:32 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb81459aaa89ddb4457649e4f58109d7772dd1d1a7d0b1a62d8abe9aeaaf71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575fe32252544df19b953020b7d552550f2bfa39282d078e8fc68ba9dac9626a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 22 Jan 2024 14:26:01 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1eb2186e5388f5b1a4e87b35d30282c0e70acc932b195bcddd90461ba6743d`  
		Last Modified: Wed, 14 Feb 2024 00:58:04 GMT  
		Size: 143.7 MB (143720411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cccb62ce0c4678fef06eb6a3614009b83081e2897dcbbd343851d3c46ec179`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05537327b703d25078ee37777017c6934663947777c3b7b1f7b71ef952166f3c`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a820a35ee158ccc7944ea480546c8497168dd04ae914e99688642c649df42fff`  
		Last Modified: Wed, 14 Feb 2024 01:10:45 GMT  
		Size: 371.4 MB (371390905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f7342bb794f3536fde17c0579dfa0533ba9aace7f30a0f304c3e874f456122db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2778287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cb11b8c7d63149c24626643939aa383280fc71b30e293ddf46ba20109425fb`

```dockerfile
```

-	Layers:
	-	`sha256:6ba2cb3824399e949350d1e7f0f9f09fd166480cac74f0fc8e62bfd4f9818f1a`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 2.8 MB (2757780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1caaaf44de38650caeb0d49dc9521725e5b1d96c5a2f8056b86c639f48f3a8fd`  
		Last Modified: Wed, 14 Feb 2024 01:10:37 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json
