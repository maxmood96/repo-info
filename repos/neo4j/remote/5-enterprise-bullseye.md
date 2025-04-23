## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:a4472505b26855e151f5d2bf965ee0f65b17b09913fd374552265923b251c698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:da6f5a1c7420d171ebdc19d2dc4bb10db7e8a9409c913b00eb0429d5ef5379e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.1 MB (626140395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8d05dcc05ce54316f72e67210fe6fc8498c7086351c1abdd89d310a1aee44b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 02 Apr 2025 06:15:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 02 Apr 2025 06:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Apr 2025 06:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9a3ac5599d85f80f935bec032bdaa7e49c83f8f84f2929b3cb49ac0b3cbda82 NEO4J_TARBALL=neo4j-enterprise-5.26.5-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 02 Apr 2025 06:15:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.5-unix.tar.gz
# Wed, 02 Apr 2025 06:15:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.5-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.5-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Apr 2025 06:15:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Apr 2025 06:15:25 GMT
VOLUME [/data /logs]
# Wed, 02 Apr 2025 06:15:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 02 Apr 2025 06:15:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Apr 2025 06:15:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f5d3aa03a69d4238c1f2c322e28deabaf689dfd19241cb2fa36ee9b9deaca8`  
		Last Modified: Wed, 23 Apr 2025 17:13:50 GMT  
		Size: 144.6 MB (144634974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c52f543dff41cabc7cb7e4ca0cb809723361baff7c95fef47f890d88e2dc3c`  
		Last Modified: Wed, 23 Apr 2025 17:13:46 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc712ea3ccf745ab526dfab9738e7ad3998645d4796bfe301d1028df2c1400c5`  
		Last Modified: Wed, 23 Apr 2025 17:13:46 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e24694ecce1c516c71ed6796c1a22dceab0d13d9b5624911686c525afc077`  
		Last Modified: Wed, 23 Apr 2025 17:13:56 GMT  
		Size: 451.2 MB (451234103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:873bd213d2689a1054553430e3c39279e86b2474f438388b145c6f9bd28bbc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716a13df5c4de99208e44cbab8b133b4adf7e54c6081e1f8889d7b7611ef7ad2`

```dockerfile
```

-	Layers:
	-	`sha256:bcf22f59a67986683cfcc21f907c8a774645c82c6dd85fad4753240b859882b9`  
		Last Modified: Wed, 23 Apr 2025 17:13:47 GMT  
		Size: 3.6 MB (3562509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758ce6f8b2f29b0aa1837a86d5bf8b40b1aca856f8f5567814f91fbcff0b1c67`  
		Last Modified: Wed, 23 Apr 2025 17:13:46 GMT  
		Size: 20.8 KB (20758 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:98a1444914d227b4872400d8bc016a5412531569badb30f71073fba3d9d0cd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.5 MB (623470499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4825610cc585593a62b1ba271bcbe856271ad5b48277a657b7bbb75819c03227`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 02 Apr 2025 06:15:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 02 Apr 2025 06:15:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Apr 2025 06:15:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9a3ac5599d85f80f935bec032bdaa7e49c83f8f84f2929b3cb49ac0b3cbda82 NEO4J_TARBALL=neo4j-enterprise-5.26.5-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 02 Apr 2025 06:15:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.5-unix.tar.gz
# Wed, 02 Apr 2025 06:15:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.5-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.5-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 02 Apr 2025 06:15:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Apr 2025 06:15:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Apr 2025 06:15:25 GMT
VOLUME [/data /logs]
# Wed, 02 Apr 2025 06:15:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 02 Apr 2025 06:15:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Apr 2025 06:15:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2cbeb7de91ba4cd7ce2a6c214ea30fb41267c58cd7905c6d012910d146e1dc`  
		Last Modified: Wed, 23 Apr 2025 18:11:47 GMT  
		Size: 143.5 MB (143512631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f16bd8fa741826a95f624d7e64c074273dc1921f40f76c77a7a583f0cc363b2`  
		Last Modified: Wed, 23 Apr 2025 18:13:02 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123cd7f605f1f0a6f35e496fbb8a5784751beaafb17f4b92da0408a967f865a9`  
		Last Modified: Wed, 23 Apr 2025 18:13:01 GMT  
		Size: 10.0 KB (10025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31daf045b2618d815e83f75acbb6919861217562504cf0cecd0cede8ede256e`  
		Last Modified: Wed, 23 Apr 2025 18:13:12 GMT  
		Size: 451.2 MB (451194443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8975d5e6ca7d9d5a531e259a46daa6ae9106000a0260d8ec474efb5fd6a352a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebc50ae472931c0f9ef5d9d034254405b3bfb1adc1fb8d8184e9d4336832525`

```dockerfile
```

-	Layers:
	-	`sha256:9a507710c164e18397623077eaed0a6ff8d90f99a4740471dbfc8021a04ea37f`  
		Last Modified: Wed, 23 Apr 2025 18:13:02 GMT  
		Size: 3.6 MB (3562179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5859fcf98bfc73c8564ad453f033e15c0fd8c784a8a0767f3d4820f310af973`  
		Last Modified: Wed, 23 Apr 2025 18:13:01 GMT  
		Size: 20.9 KB (20926 bytes)  
		MIME: application/vnd.in-toto+json
