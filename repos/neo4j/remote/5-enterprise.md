## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:38dd347ec17162b025829bd16a1e4b71f9ab27e8e4429b8162b3b2165934ac6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:58c42d28afa0f292a5c787d476a346c06da96bc6a57276e8903c7c967aa03c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.1 MB (626137492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f32d3d4689fd96eac315bb58fffdd7252ef8809c4705df7fe575e3679c81e4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 02 Apr 2025 06:15:25 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ee8eec41665d980bf9812f11013839031b92539d85d159d0123d7ec2e24292`  
		Last Modified: Mon, 28 Apr 2025 22:09:25 GMT  
		Size: 144.6 MB (144634953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b93335e6035e74b1004cbcae35692d3ffeaf31a83cbf426528f69591ea8273`  
		Last Modified: Mon, 28 Apr 2025 22:09:20 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ff6f18d8b38426f4757bb96ee0ad01ef07dfd6aa68382d0b7da555735ac89a`  
		Last Modified: Mon, 28 Apr 2025 22:09:20 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e80dfa62823849eb89ebeff016e8de45715c1acf664feac573bc99e8622ec10`  
		Last Modified: Mon, 28 Apr 2025 22:09:30 GMT  
		Size: 451.2 MB (451234040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e208106862cfa426437f04cde625c4f0b2916f13d9fd098b85a714de514c6458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e82b10789808b4801f717bef60730af86ffa01299b9cc340d96cbb83c741a9`

```dockerfile
```

-	Layers:
	-	`sha256:436c0d6328a0bc0593f24d6c2dfdd113690bcae95b923ecb08c49f740e58e5b9`  
		Last Modified: Mon, 28 Apr 2025 22:09:20 GMT  
		Size: 3.6 MB (3562563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6405205ca675dae8eb871c138b7dea4d8fcdf08d80c064d32a4a7a1be03be5ec`  
		Last Modified: Mon, 28 Apr 2025 22:09:20 GMT  
		Size: 20.8 KB (20758 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2fafdbba839aa55a3ab7f113cf7a16314e211fa46c7b2d0a0d212c4e0a8e7042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.5 MB (623465716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498fa727d5e14dc4cfcdd1cf8540c85aeeefbd625f017f23298f1ef5f8cf0c7e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 02 Apr 2025 06:15:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72262fe32b026e7f23e9a38bfb2a66973be30355ac7b2a0fe73a91bfb575d0f`  
		Last Modified: Tue, 29 Apr 2025 20:15:14 GMT  
		Size: 143.5 MB (143512633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da118ceb8400d31cb52949ad9dc9fd5970e528d1e594e6321516af93b4630444`  
		Last Modified: Tue, 29 Apr 2025 20:15:10 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86db03fe736e67c0bda3c2f38a7a0ff856ae0eb4fa08df9a4ada12163f0ce1c1`  
		Last Modified: Tue, 29 Apr 2025 20:15:10 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45413813ccb12482e2cd781b9b2ce7ecb67a5011c2500d0c4a7626ae2d9f0cd0`  
		Last Modified: Tue, 29 Apr 2025 20:15:20 GMT  
		Size: 451.2 MB (451194511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b17b5c57b1a969bda0f8dc96d1beb44a0865cf80772c41e309b64369300f7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844687ed5f26143bf3ef40960d5bbf2b362703ebd9e932fea208c5a3bf9a698d`

```dockerfile
```

-	Layers:
	-	`sha256:51e0b1418df6b694fb5f0beefa40d3b8c25c64ae4a35df240f69c8cd210870a9`  
		Last Modified: Tue, 29 Apr 2025 20:15:11 GMT  
		Size: 3.6 MB (3562233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90f4dae97fb79ee779bc4239fcf0794b34fb6ec92b0694202eb1e755c8ce014`  
		Last Modified: Tue, 29 Apr 2025 20:15:10 GMT  
		Size: 20.9 KB (20926 bytes)  
		MIME: application/vnd.in-toto+json
