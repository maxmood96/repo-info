## `crate:latest`

```console
$ docker pull crate@sha256:b52c7f22b0affab212a03992a372373a6bd0fb20e73f195457c601ab0f41f6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:8a88846d24bfd57686b13763625fd740818312640b734fb32a3235bdee81e8e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350984906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e82ce545128e3e6d44851caf6fb5cf10da40ae50da92db7fa420ea9e41eebf1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 12 Nov 2019 02:25:33 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 05 Feb 2020 23:25:54 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 05 Feb 2020 23:25:54 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Wed, 05 Feb 2020 23:25:55 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Tue, 18 Feb 2020 23:19:53 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.2.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.2.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.2.tar.gz.asc crate-4.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.2.tar.gz.asc     && tar -xf crate-4.1.2.tar.gz -C /crate --strip-components=1     && rm crate-4.1.2.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Tue, 18 Feb 2020 23:19:53 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Feb 2020 23:19:54 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Feb 2020 23:19:56 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Feb 2020 23:19:56 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2020 23:19:56 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Feb 2020 23:19:57 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Feb 2020 23:19:57 GMT
VOLUME [/data]
# Tue, 18 Feb 2020 23:19:57 GMT
WORKDIR /data
# Tue, 18 Feb 2020 23:19:57 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Feb 2020 23:19:58 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Feb 2020 23:19:58 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Feb 2020 23:19:58 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-02-14T15:29:55.666729 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.2
# Tue, 18 Feb 2020 23:19:58 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Tue, 18 Feb 2020 23:19:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2020 23:19:59 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82aa4130eb2a175e62f98b2ce60e9b2e0d68d8ae342810b26c821bedc428983`  
		Last Modified: Tue, 12 Nov 2019 02:30:36 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c132278b93b3443fafff8460382be10690caf0702bc22339ea0dd7b81d5cf8b`  
		Last Modified: Wed, 05 Feb 2020 23:31:07 GMT  
		Size: 196.4 MB (196423227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42807ee70d40e75fddd4f32ee923cedd85714cfe1339b0e13e317438a447e721`  
		Last Modified: Wed, 05 Feb 2020 23:28:42 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e857f3ea43836a8db4dff8ae8260b00e4c825b16ad1c67cb6eb049d1542c34e`  
		Last Modified: Tue, 18 Feb 2020 23:20:28 GMT  
		Size: 77.5 MB (77481382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa3cafdae1232c07738e4653bafe888ba8c300102508e49eb895263747b04ff`  
		Last Modified: Tue, 18 Feb 2020 23:20:21 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177f0cc0af379ce0345739fe6b807fad9bf2d259b63d327c46c72642842fa4c5`  
		Last Modified: Tue, 18 Feb 2020 23:20:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822a9eedbca0684494b262599d5c8ac98872f8cfdda86e37be38b1ce236d5811`  
		Last Modified: Tue, 18 Feb 2020 23:20:20 GMT  
		Size: 1.3 MB (1294051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8398841f691af2b4cead17276af3d86814536d5656a1df1b2839ae82006f4a7a`  
		Last Modified: Tue, 18 Feb 2020 23:20:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf15fea133792ed2c5dfb8c066c544ce305945b119cafa58f5a80732b0b6e2d`  
		Last Modified: Tue, 18 Feb 2020 23:20:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a672850ce4d4f5b97d1e7fd61c10b9137c09e093ca63fee694832e79cf704640`  
		Last Modified: Tue, 18 Feb 2020 23:20:19 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b78a5fafee7c82f0c5980b4047cad16334a89c5dcbdb9968f8f6fef9fe10314`  
		Last Modified: Tue, 18 Feb 2020 23:20:19 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:bb436511838da5c89464e526e9df835f7071b6924a063a50ae13e2b8a9da5c99
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.5 MB (376518736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3497accaa760c2f0c983af7ab14457c862d0167f9c05f422df3e3bdb4cf458`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Tue, 12 Nov 2019 00:40:03 GMT
ADD file:8449a578596d0a7b4ce64f74355f602ee47b1a8782058356ae614cdcdf4639fb in / 
# Tue, 12 Nov 2019 00:40:05 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:40:06 GMT
CMD ["/bin/bash"]
# Wed, 05 Feb 2020 23:45:29 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 05 Feb 2020 23:46:15 GMT
RUN curl --retry 8 -o /openjdk.tar.gz https://download.java.net/java/GA/jdk13.0.1/cec27d702aa74d5a8630c65ae61e4305/9/GPL/openjdk-13.0.1_linux-x64_bin.tar.gz     && echo "2e01716546395694d3fad54c9b36d1cd46c5894c06f72d156772efbcf4b41335 */openjdk.tar.gz" | sha256sum -c -     && tar -C /opt -zxf /openjdk.tar.gz     && rm /openjdk.tar.gz
# Wed, 05 Feb 2020 23:46:17 GMT
ENV JAVA_HOME=/opt/jdk-13.0.1
# Wed, 05 Feb 2020 23:46:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts /opt/jdk-13.0.1/lib/security/cacerts
# Tue, 18 Feb 2020 22:40:17 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.2.tar.gz     && curl -fSL -O https://cdn.crate.io/downloads/releases/crate-4.1.2.tar.gz.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.1.2.tar.gz.asc crate-4.1.2.tar.gz     && rm -rf "$GNUPGHOME" crate-4.1.2.tar.gz.asc     && tar -xf crate-4.1.2.tar.gz -C /crate --strip-components=1     && rm crate-4.1.2.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3     && ln -sf /usr/bin/python3.6 /usr/bin/python
# Tue, 18 Feb 2020 22:40:20 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Feb 2020 22:40:20 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Feb 2020 22:40:24 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.24.2.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.24.2.asc crash_standalone_0.24.2     && rm -rf "$GNUPGHOME" crash_standalone_0.24.2.asc     && mv crash_standalone_0.24.2 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Tue, 18 Feb 2020 22:40:25 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2020 22:40:25 GMT
ENV CRATE_HEAP_SIZE=512M
# Tue, 18 Feb 2020 22:40:27 GMT
RUN mkdir -p /data/data /data/log
# Tue, 18 Feb 2020 22:40:28 GMT
VOLUME [/data]
# Tue, 18 Feb 2020 22:40:28 GMT
WORKDIR /data
# Tue, 18 Feb 2020 22:40:29 GMT
EXPOSE 4200 4300 5432
# Tue, 18 Feb 2020 22:40:29 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Tue, 18 Feb 2020 22:40:30 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Tue, 18 Feb 2020 22:40:30 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2020-02-14T15:29:55.666729 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.1.2
# Tue, 18 Feb 2020 22:40:31 GMT
COPY file:9830363b41b8063591887d9dc9ce2767bf0e91dc4cb05efcb6ea622a60ec15e3 in / 
# Tue, 18 Feb 2020 22:40:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 18 Feb 2020 22:40:32 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:3f2696f8166ff69dd0c116674b19eebd351ed3fc4111a42dbd57c673601c725d`  
		Last Modified: Tue, 12 Nov 2019 00:40:46 GMT  
		Size: 103.6 MB (103619629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e11d48e7bd36dbc63110f197eefe11eb9a4f505370153c386e5938d14144b04`  
		Last Modified: Fri, 07 Feb 2020 17:42:20 GMT  
		Size: 2.3 KB (2262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d6743359dfaf8645137afd31a4552eb3195971517a48fca57593b25250b015`  
		Last Modified: Tue, 18 Feb 2020 22:42:08 GMT  
		Size: 196.4 MB (196423249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf4a3a653abc3f2a5931326c03e9ef927aec2a7ab30aa4fcc311b69d41fa57c`  
		Last Modified: Tue, 18 Feb 2020 22:41:34 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:412e3956cb94a0e820971a83b3b541bba1b7e02310b0ab6dc1390d2dfe708988`  
		Last Modified: Tue, 18 Feb 2020 22:41:48 GMT  
		Size: 75.2 MB (75176207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bc7e61961f2d7311bcfbcd311dd0b0672f6c0c7b7ce219c7f1e1e4c4155433`  
		Last Modified: Tue, 18 Feb 2020 22:41:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c9c19aac6ea5aa9a6c1554f9d9213c0df72055c9b79581e4e37bf328a677ef`  
		Last Modified: Tue, 18 Feb 2020 22:41:34 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ec61ec0c4d88f7a245aa67ab7511cf00f8a8df324ff0781037ffd3d25727b4`  
		Last Modified: Tue, 18 Feb 2020 22:41:33 GMT  
		Size: 1.3 MB (1294049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074bffcd445bfa98fd8e6db58b9fa694a16b400e9de626101f3916d9f738f66e`  
		Last Modified: Tue, 18 Feb 2020 22:41:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b62b9b0d96da53092c8fe41686a5d7e37e3280aae8a91d94dbeff67dd0c3b`  
		Last Modified: Tue, 18 Feb 2020 22:41:32 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81794e883731785f8b58bc50495ea7de54da4437eeb8bf25125f4017c2670c61`  
		Last Modified: Tue, 18 Feb 2020 22:41:32 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ec1f342b6aab7f60393088704c391077a0a6a66b563c5c631be463e9f15347`  
		Last Modified: Tue, 18 Feb 2020 22:41:32 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
