## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:f4788d62ebc21b8195bf7e356924e13278b4c7474085e2fdd31128f2997489d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:62dbafb30f411d22f9b685203f5b43a1774628f45e2bbe8a47a951a634ddf899
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564632471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb77f13c1c06a5573ca6b76f9b0b6dac1b8ca75780013a9db8e8dec26f911f6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 07:35:48 GMT
COPY dir:e13dbcd57950f4d4d23f4aba8428b6fbbf838d8f4801d32a25e344d37d33c37e in /opt/java/openjdk 
# Sat, 02 Dec 2023 07:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63e73f347697cab2b2e13b434c71e0116e87d4e11227dba878eb288300f47e7c NEO4J_TARBALL=neo4j-enterprise-5.14.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 02 Dec 2023 07:36:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
# Sat, 02 Dec 2023 07:36:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 02 Dec 2023 07:36:34 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 02 Dec 2023 07:37:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Sat, 02 Dec 2023 07:37:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 07:37:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 02 Dec 2023 07:37:19 GMT
VOLUME [/data /logs]
# Sat, 02 Dec 2023 07:37:19 GMT
EXPOSE 7473 7474 7687
# Sat, 02 Dec 2023 07:37:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 02 Dec 2023 07:37:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4929994d0853caabbfd68ce7ab07e3af7c0e483db2f66881247df513f25c95`  
		Last Modified: Sat, 02 Dec 2023 07:40:56 GMT  
		Size: 144.9 MB (144873901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9cb55318b889d800ca28685c3b305c2b3b3e8d4a84b51be72d0802ee8669c4`  
		Last Modified: Sat, 02 Dec 2023 07:41:38 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2d94ca0b5033c8422e83b285e4c4076035849d43c71cacd043b996c949212d`  
		Last Modified: Sat, 02 Dec 2023 07:41:38 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b1c60951a456bd38d0f92b48949bd8d248883ab89b374415573d908027651b`  
		Last Modified: Sat, 02 Dec 2023 07:41:53 GMT  
		Size: 388.3 MB (388327398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:38e26208bdaf43907adf3b729c8ad9d7359a25d779fbcc771eae69a3ce54bf9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011222cf93171c66aa6789fcdcded634920296bb7de05368e156ab333e8c643`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:54:33 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Fri, 15 Dec 2023 19:54:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 15 Dec 2023 19:54:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Fri, 15 Dec 2023 19:54:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 15 Dec 2023 19:54:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Fri, 15 Dec 2023 19:54:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Fri, 15 Dec 2023 19:54:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:54:48 GMT
WORKDIR /var/lib/neo4j
# Fri, 15 Dec 2023 19:54:48 GMT
VOLUME [/data /logs]
# Fri, 15 Dec 2023 19:54:48 GMT
EXPOSE 7473 7474 7687
# Fri, 15 Dec 2023 19:54:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 15 Dec 2023 19:54:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d93fb72555944d51d7e18e85dbba1405725af6fa11dc155f20ab3dc455df52`  
		Last Modified: Sat, 02 Dec 2023 09:08:50 GMT  
		Size: 143.7 MB (143681749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfda03cc0832011a22b20addea2402464befa486f7f25ccce0fbac8fc1a5d5e8`  
		Last Modified: Fri, 15 Dec 2023 19:58:22 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d952aa4ac391ad27a65ecc9fd7b1d9037b26d856a359961575e8ee3acf304b3`  
		Last Modified: Fri, 15 Dec 2023 19:58:21 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbe77bbe7384be2f06a8114b7dffd3ada2dddc79443b666f1694301b2cdf296`  
		Last Modified: Fri, 15 Dec 2023 19:58:35 GMT  
		Size: 389.4 MB (389403382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
