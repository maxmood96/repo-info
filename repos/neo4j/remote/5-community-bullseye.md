## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:269ab39c0459ea09befbbde586f3a2033e2339afe4bc10951e6bf827b00c275c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:83f60aaf60698a9a79ddeb436ff0e2b1488ac3de2e92576da3600d9da4375b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304209755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfde9e154a491e51cc8961406e91756544fe1e035af8d18e8e15763f48ac0f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 13:55:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 13:55:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=80ae623641a3b353e3b2bca5e49cb6f0dbb79d89d512850c751c356a1378c444 NEO4J_TARBALL=neo4j-community-5.22.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 23 Jul 2024 13:55:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 13:55:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 Jul 2024 13:55:16 GMT
VOLUME [/data /logs]
# Tue, 23 Jul 2024 13:55:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 23 Jul 2024 13:55:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93434bba57c4205f8008506bc59dff4f894a61f081a138f9fa8fe4540c3ff07c`  
		Last Modified: Tue, 23 Jul 2024 18:14:11 GMT  
		Size: 145.2 MB (145166533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a7b513e7443aa7b2fd1c8634ff4e2518bf57e76a61f9e3726fd617791de33`  
		Last Modified: Tue, 23 Jul 2024 18:14:07 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bab337b0425aacf8de629d1f4b3360333778d6140b39012c458160ad00aab92`  
		Last Modified: Tue, 23 Jul 2024 18:14:07 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fc1b4f9dd9ac8d83be8eb39b9d91e393e420d3dd0d78189f9de5279236dbc4`  
		Last Modified: Tue, 23 Jul 2024 18:14:11 GMT  
		Size: 127.6 MB (127601396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9cb74f837092c86ea4b29b7d3d8bd5c58501c0ceb231b4f3c843dc7aa9bd5536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3051076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5956a48deb42e2c602300606738f55f2a23ce7d9374e0868d12748039cbf9f2`

```dockerfile
```

-	Layers:
	-	`sha256:113f48a05fedc4931b81a98954546d75171d43adca9932d14833aa331ca25dd8`  
		Last Modified: Tue, 23 Jul 2024 18:14:07 GMT  
		Size: 3.0 MB (3027693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14258504adddaa8864a03edfef82cfac390b4581f6be8777aaa86cd84c573ad2`  
		Last Modified: Tue, 23 Jul 2024 18:14:07 GMT  
		Size: 23.4 KB (23383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ef9c719ef30f8334014a6286baa062c9988be8eb3dafda8ff5e5d32f4e510b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301614198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c501a62ca994677c35082fc040a26abcc3d24dfc760c877734a25dd1bf9f4f47`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 13:55:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 13:55:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=80ae623641a3b353e3b2bca5e49cb6f0dbb79d89d512850c751c356a1378c444 NEO4J_TARBALL=neo4j-community-5.22.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 23 Jul 2024 13:55:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.22.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 13:55:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 Jul 2024 13:55:16 GMT
VOLUME [/data /logs]
# Tue, 23 Jul 2024 13:55:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 23 Jul 2024 13:55:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c6c94bfde96f39c9817ef48cc71540647b81caced404855315c4e47530ceae`  
		Last Modified: Wed, 24 Jul 2024 12:50:33 GMT  
		Size: 144.0 MB (143959485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4510874c54c166d5ab3d1b7c5934197e94f9944fd29ed25047a279f44250b45e`  
		Last Modified: Wed, 24 Jul 2024 12:50:29 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262e5d92549097aab501f1a3603345131558fdb2919838af48d2fdf3c4b8b456`  
		Last Modified: Wed, 24 Jul 2024 12:50:29 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f592ef83e04cd6f159a8881a2464be89d0feb4e83c990e5903097f432c71c53`  
		Last Modified: Wed, 24 Jul 2024 12:50:33 GMT  
		Size: 127.6 MB (127565102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:05c2c83afd745b8b45c0143cc1ceda5099a486d60db87bd6aa8b5deee61eb4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3052181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7cff4182278ab83dc54b1082bacbf299eac5bc09b288e618021c93859c1c07`

```dockerfile
```

-	Layers:
	-	`sha256:e3738e42d1e9c07d62395819c0a8c74039a1da6afd8ba3025214b7eff2701dab`  
		Last Modified: Wed, 24 Jul 2024 12:50:30 GMT  
		Size: 3.0 MB (3028100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8686ec82b8c0eb6c6f0c10f564f209d985bd978eec6631e0f1f4cdb4dbf417a5`  
		Last Modified: Wed, 24 Jul 2024 12:50:29 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json
