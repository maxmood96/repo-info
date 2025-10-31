## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:c5c82b81d6a844b882f916fa86bb8447d2f753aa7e3df843675dd7fac155ffcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ae580a8bde99f746c90cc7536b6e878ee1fc49597ce0b946f2d97e8c8d23b968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.7 MB (667698523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9906db043c86bd1c6be7f90b63c7f46cc06d5f55df71475c13532e854971c9e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 20:50:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Oct 2025 20:50:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Oct 2025 20:50:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a6863f38852aa5d38c4e71c061ef0a6b6ffa453aa4c4a7481b0d1813fcbdcebf NEO4J_TARBALL=neo4j-enterprise-5.26.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 30 Oct 2025 20:50:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.15-unix.tar.gz
# Thu, 30 Oct 2025 20:50:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 30 Oct 2025 20:50:07 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 30 Oct 2025 20:50:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.15-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 30 Oct 2025 20:50:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 20:50:45 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Oct 2025 20:50:45 GMT
VOLUME [/data /logs]
# Thu, 30 Oct 2025 20:50:45 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 30 Oct 2025 20:50:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 30 Oct 2025 20:50:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532bf6919629c72417664b447099aa3bbb0eb9fb8f7f0cf41fc30b15c025181f`  
		Last Modified: Thu, 30 Oct 2025 23:48:38 GMT  
		Size: 144.7 MB (144693318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c55f4c553b5bf5eb45799f6881ea553db4ed5be7ed8362250b14da06266e3`  
		Last Modified: Thu, 30 Oct 2025 20:51:34 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f44ec8256dea1463cf98b54f344c6b2d7636c4c3c623cc60d967642ac36e2d`  
		Last Modified: Thu, 30 Oct 2025 20:51:34 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbed048e39c6ec05641540866f3b3b1680dfcab7d5707ea2780c4b114a0c5388`  
		Last Modified: Thu, 30 Oct 2025 23:46:40 GMT  
		Size: 492.7 MB (492732904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:335500ba09e9d6644bf12f086a1ecfac255d57b531f44748f5cc84a072b246b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4864195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e30ad21a85b74aaf6b6552f4c9468d4d4dafdeb5edc8ff846af6a12fddec402`

```dockerfile
```

-	Layers:
	-	`sha256:07e8c6c222a674c69c88cf44681124346c1678c1660d8811a2964335d2583d03`  
		Last Modified: Thu, 30 Oct 2025 23:44:59 GMT  
		Size: 4.8 MB (4843210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c34b6407e8e60960acaedab25cdca9f2ac1c0c0dd5698cd8220749e88cfed4`  
		Last Modified: Thu, 30 Oct 2025 23:45:00 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d599508962a29147417c1b50aa017736649deef5a21f0851c9db350cd9f0005a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.3 MB (664281444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3d634c2eda7aa663c31c22336fbda58204f02d85632076c006e9c2e612f56e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 20:51:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Oct 2025 20:51:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Oct 2025 20:51:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a6863f38852aa5d38c4e71c061ef0a6b6ffa453aa4c4a7481b0d1813fcbdcebf NEO4J_TARBALL=neo4j-enterprise-5.26.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 30 Oct 2025 20:51:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.15-unix.tar.gz
# Thu, 30 Oct 2025 20:51:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 30 Oct 2025 20:51:29 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 30 Oct 2025 20:51:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.15-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 30 Oct 2025 20:51:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 20:51:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Oct 2025 20:51:52 GMT
VOLUME [/data /logs]
# Thu, 30 Oct 2025 20:51:52 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 30 Oct 2025 20:51:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 30 Oct 2025 20:51:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8227007da1c461b87a51ed5098d4b3151239ccf5e2d121adc17f8a68a2591a`  
		Last Modified: Thu, 30 Oct 2025 23:59:34 GMT  
		Size: 143.5 MB (143542161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5c3bdf3fee933ef48bfb886452c839075fd9c0f959976ab7ea21ce736d4967`  
		Last Modified: Thu, 30 Oct 2025 20:52:40 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cbbed56a61975491087abdeb4aa92398c6ac00449c9db45ad7c0bec74b7aae`  
		Last Modified: Thu, 30 Oct 2025 20:52:40 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d4c8ca952ec2aa0e2a6945c97294d65c179867e9a20f346b3a983214704f22`  
		Last Modified: Thu, 30 Oct 2025 23:59:50 GMT  
		Size: 492.0 MB (491976917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2f6ec17a6d6d0e4c2eb98184be3c55d78f331fbfb82c5534b822f731c6a89b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4838169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:132ae0ae18c7911e544f618bf87e0511a2a0d27bca58bd6f9f86684b37fda13f`

```dockerfile
```

-	Layers:
	-	`sha256:9e2833712ef8cb35dcb088583fa958414d9371c90c47f335e638ab68342eb4d0`  
		Last Modified: Thu, 30 Oct 2025 23:45:05 GMT  
		Size: 4.8 MB (4817015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838df194496da2fa30e6e62eec8a757c49e7a580eea63fa98096e443f4dcf009`  
		Last Modified: Thu, 30 Oct 2025 23:45:06 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json
