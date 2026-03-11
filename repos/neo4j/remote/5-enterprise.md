## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:b23958230f10cee0716a81942686d0ef2060dbe841e542005f811880102ca803
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:35a00d55092c91ee3c041abf29c89c02d2ccbdfb9926aae06dd44805194a2319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.4 MB (706441239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890268678a364862fceeed23a919b2fc361a81b9b04861b98b427e7d7e8f40e0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:37:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Mar 2026 22:37:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Mar 2026 22:37:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=72fd5f116ab82e853661c644ae6de36548cb38e0c0bc237b1e766aec5b123194 NEO4J_TARBALL=neo4j-enterprise-5.26.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Mar 2026 22:37:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.22-unix.tar.gz
# Tue, 10 Mar 2026 22:37:07 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Mar 2026 22:37:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.22-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Mar 2026 22:37:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 22:37:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Mar 2026 22:37:38 GMT
VOLUME [/data /logs]
# Tue, 10 Mar 2026 22:37:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Mar 2026 22:37:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:37:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce57b50fdddee9413474b2d58c832f9b41763363f9b2645b9dcdd64453ddb683`  
		Last Modified: Tue, 10 Mar 2026 22:38:13 GMT  
		Size: 157.9 MB (157857123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f24e1df91fc26b4e80aa374d706377d6c1417a4f6b66202f760acb3ad7fa3`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834149149aa127c550bb9be82817dd3530451b2797cb3bc5780596aee6ac4f33`  
		Last Modified: Tue, 10 Mar 2026 22:38:22 GMT  
		Size: 518.8 MB (518795390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2cfd27a4e06b657ddfd14942b86fc55d62a02e7df29952a88b91b1141d9210a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4671072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6594119be80d5fe7071e46b51d95d2b4a17ef2bb4f1c96f3842e80b0c0bc0c4`

```dockerfile
```

-	Layers:
	-	`sha256:8d0b9072e662987d4ba0501ea0a92e68e36affac914667e2f1e511dd00e9acf7`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 4.7 MB (4651775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f837992101d20a191f1cbfa72961fddddbaf001b99bc8ba5e73c5135f34b4e`  
		Last Modified: Tue, 10 Mar 2026 22:38:08 GMT  
		Size: 19.3 KB (19297 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e548cb6ac1063a56d4008201d6327cf6948f0e4d241f3b314fce1f8f8fbf393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.1 MB (704147192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0704491926f4f40bc949cc9365fd52753199fb580d8a7fc0e32e1e7d5e7c8420`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:36:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Mar 2026 22:36:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Mar 2026 22:36:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=72fd5f116ab82e853661c644ae6de36548cb38e0c0bc237b1e766aec5b123194 NEO4J_TARBALL=neo4j-enterprise-5.26.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Mar 2026 22:36:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.22-unix.tar.gz
# Tue, 10 Mar 2026 22:36:48 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Mar 2026 22:37:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.22-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Mar 2026 22:37:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Mar 2026 22:37:33 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Mar 2026 22:37:33 GMT
VOLUME [/data /logs]
# Tue, 10 Mar 2026 22:37:33 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Mar 2026 22:37:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:37:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8d72080d44a8b4aaffa0321a533b219d3e2ab00836506a9784373de3a5f688`  
		Last Modified: Tue, 10 Mar 2026 22:38:10 GMT  
		Size: 156.1 MB (156133065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a398ebc68bee214babd03dc19dde9c296148320e733242397f5ff134c60c2cd4`  
		Last Modified: Tue, 10 Mar 2026 22:38:04 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02618be6ba2c11404816dc91cdde80a9883ec29c85d8c85fcfb794c9066022f`  
		Last Modified: Tue, 10 Mar 2026 22:38:18 GMT  
		Size: 517.9 MB (517863936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:9ef02e1d80299c46c609713275fd7ecb5ac051d8f1411c928b768ce1af48ef4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4665680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e910ea26c420effea1455505d467253809c20a1387d0ce1fc0ea12e6d51645`

```dockerfile
```

-	Layers:
	-	`sha256:211d0ddda537594aab2cc150af59f991ecdeadcad5c5e159e669e908e1350ef0`  
		Last Modified: Tue, 10 Mar 2026 22:38:04 GMT  
		Size: 4.6 MB (4646229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5ff1cfec105d544883f2a3ec3b3cb3106dbfb567bbaa227855eeb78d829fa40`  
		Last Modified: Tue, 10 Mar 2026 22:38:04 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json
