## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
