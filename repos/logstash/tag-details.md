<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.16`](#logstash81916)
-	[`logstash:9.3.5`](#logstash935)
-	[`logstash:9.4.2`](#logstash942)

## `logstash:8.19.16`

```console
$ docker pull logstash@sha256:f50650a7c125c6b054631064ea353fabdb5a7258b2f8e8f7baffd88a6cdfc764
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.16` - linux; amd64

```console
$ docker pull logstash@sha256:fa6a9e14de1443f70dc96b04f8705dc4bc977160fb9dc9ad6b5ad3f676f9b315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.8 MB (542757194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ae6142ec3d667306679b59839d2ecd15b2ba7baaf6bf6f7a0bd66c87dea5f4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:19:00 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 02 Jun 2026 08:19:01 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 02 Jun 2026 08:19:42 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.16-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.16 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Jun 2026 08:19:42 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Jun 2026 08:19:42 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 08:19:42 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:19:42 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 02 Jun 2026 08:19:42 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 02 Jun 2026 08:19:42 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 02 Jun 2026 08:19:43 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 02 Jun 2026 08:19:43 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:19:43 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 02 Jun 2026 08:19:43 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 02 Jun 2026 08:19:43 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Jun 2026 08:19:43 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:19:43 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 02 Jun 2026 08:19:43 GMT
USER 1000
# Tue, 02 Jun 2026 08:19:43 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Jun 2026 08:19:43 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.16 org.opencontainers.image.version=8.19.16 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-05-23T16:24:56+00:00 org.opencontainers.image.created=2026-05-23T16:24:56+00:00
# Tue, 02 Jun 2026 08:19:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feffee925ed4abccbe235f59b76114fbc50b5e15d0ab5a1a77d344353fc6e033`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 55.0 MB (55015771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6e1ebbc495162dfe45891fea62bf849ae6453b3272593c0624dffb699dd22`  
		Last Modified: Tue, 02 Jun 2026 08:20:17 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b78c8c42777e23cd476fbdfd62cf107d5bce37537bcc3579fd16462404380d`  
		Last Modified: Tue, 02 Jun 2026 08:20:28 GMT  
		Size: 457.7 MB (457740883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668c9da7eb2fe54e261ac214225711f050b57981e649e971e5e425a30e895c5f`  
		Last Modified: Tue, 02 Jun 2026 08:20:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ad13a3aba31b50dadf8a8b319219828f9ace21eed280f5da1e91cc64aeeabc`  
		Last Modified: Tue, 02 Jun 2026 08:20:18 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32262476c8577a351547e8c4ef356742c86056ff147b5bce7433b4569ca030f0`  
		Last Modified: Tue, 02 Jun 2026 08:20:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d9f2ee56298af174d9976cc11125b12b3191fb2155818916df721ceb908434`  
		Last Modified: Tue, 02 Jun 2026 08:20:20 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7cd8ac9e7b193fff323f2d3d0707cc594356fb787f280eeea18c6fe06e299`  
		Last Modified: Tue, 02 Jun 2026 08:20:20 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ea5f1e5f4931081cb4690deba4ae281b5e6c9bc5a34c4fc94c4e0d42ec41ea`  
		Last Modified: Tue, 02 Jun 2026 08:20:21 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337aa60e4b5b9080fac8b94e31720180dd527117c751b5110cec4a761e8f3ed3`  
		Last Modified: Tue, 02 Jun 2026 08:20:21 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98675c36ea4435f30917405408b774858a7de7af53c6aa34009102c1e931b1ab`  
		Last Modified: Tue, 02 Jun 2026 08:20:22 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.16` - unknown; unknown

```console
$ docker pull logstash@sha256:64bd31e4f8f0e9fe0afaf0a65409b7df87a0f55ae1b33f6ab3d081c90271d12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5150b891ee27cd0379ef298b6c1b1d9de66206ded2a4783348254f49fcf7c2d7`

```dockerfile
```

-	Layers:
	-	`sha256:c26781ae6e79f42e18fe09f65989452c3e4e54379b0da1a58b74dbfd4664c6a4`  
		Last Modified: Tue, 02 Jun 2026 08:20:17 GMT  
		Size: 3.7 MB (3694079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e6c78294bff4f58f69ae083c1acfe65760f78bc55067715fe086e1e631c0944`  
		Last Modified: Tue, 02 Jun 2026 08:20:17 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.16` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:43e4aae58891307cb51477f2392702a3b1a24a3ee96f0d47e5f40b0c24e601f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.7 MB (543707021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8003e9d1eb1f90d334c8dffdb2ed04f434b597e015d73de605a47ab93959b228`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:19:10 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 02 Jun 2026 08:19:10 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.16-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.16 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Jun 2026 08:19:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 08:19:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:19:54 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:19:54 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 02 Jun 2026 08:19:54 GMT
USER 1000
# Tue, 02 Jun 2026 08:19:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Jun 2026 08:19:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.16 org.opencontainers.image.version=8.19.16 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-05-23T16:24:56+00:00 org.opencontainers.image.created=2026-05-23T16:24:56+00:00
# Tue, 02 Jun 2026 08:19:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2c3834116d704e70180c4f3e5346c561c391619cbcda7b4c3722c2c5fb5af5`  
		Last Modified: Tue, 02 Jun 2026 08:20:35 GMT  
		Size: 58.5 MB (58522627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467cf611640331dc6db0b5d46d0d113d79bf45c15bd1a2d1513a7443981956a`  
		Last Modified: Tue, 02 Jun 2026 08:20:32 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ce6e150dd67d4127b003fbad0e349b6bd6ac92ae2419895a3d220a794ea2c`  
		Last Modified: Tue, 02 Jun 2026 08:20:41 GMT  
		Size: 456.0 MB (456040234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefd47407f18dce3a6a09436baf7c6da4eb2c28580091c364931f8b08aed85ad`  
		Last Modified: Tue, 02 Jun 2026 08:20:32 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d3c0572f0891863cbe5524e00e1351136e9dbdd7df0f10c57151d87fc2078d`  
		Last Modified: Tue, 02 Jun 2026 08:20:33 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9845b3e910f952ffa93f7815499f5fa9102e0fb7b9ee5d6e6051aa979d4eb9cc`  
		Last Modified: Tue, 02 Jun 2026 08:20:33 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34385f8d4cb0bb26dd3e53726350b4022b16eff49dd8f169e062e7b8e473bd28`  
		Last Modified: Tue, 02 Jun 2026 08:20:35 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f638c2a238c66c8ac79afc1779bfe22e0b6364f23c42e697af9b45c0f8a4128`  
		Last Modified: Tue, 02 Jun 2026 08:20:35 GMT  
		Size: 6.3 KB (6300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64e75e284fe38f67401e8de62a44befbacd0836acd5d23c0123a911be77d86d`  
		Last Modified: Tue, 02 Jun 2026 08:20:36 GMT  
		Size: 255.2 KB (255190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cbf5e22a85b8f3a87048e6acbc9d0be73beecb854bb6a786869f7012bc7b4e`  
		Last Modified: Tue, 02 Jun 2026 08:20:36 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee019c5178a2b5368a63bc8fdea7b07ed1610f45d2a6ae3caa2c2a89720000ee`  
		Last Modified: Tue, 02 Jun 2026 08:20:36 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.16` - unknown; unknown

```console
$ docker pull logstash@sha256:5e1b60594e48d9b26c9d998a2d0c172a5b78f4364a0c01e687bffd0b0175889f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52fd5f82d40250aa031d8be9d5b72424795de56b0692d0c4f2a1396f76f5721`

```dockerfile
```

-	Layers:
	-	`sha256:1c022fdbe45ee43334b13aac476b50ccc3d346de2cb6bb63ef0963b3f62d4177`  
		Last Modified: Tue, 02 Jun 2026 08:20:32 GMT  
		Size: 3.7 MB (3694504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea8892f2406b73fec1747186560e1a10ab268446a670c2dece42a326509c5629`  
		Last Modified: Tue, 02 Jun 2026 08:20:32 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.5`

```console
$ docker pull logstash@sha256:99c7737fee9e1b32edcd81174ff8246297a2cb3e1b2e3ba436b70a6046dbc447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.5` - linux; amd64

```console
$ docker pull logstash@sha256:9094b1ad5cffb93210b37cd9d6f9d853ecae602f99c03b983d5eec816eaa22a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.0 MB (517999210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d0621e0ef520a7483a9048abbdbcf4713232d9b41472dc86599f560ba98a51`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:15:03 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:15:03 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:15:03 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:15:03 GMT
WORKDIR /usr/share
# Mon, 15 Jun 2026 23:15:05 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:15:36 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 15 Jun 2026 23:15:36 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 15 Jun 2026 23:15:36 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 15 Jun 2026 23:15:37 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 15 Jun 2026 23:15:37 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 15 Jun 2026 23:15:37 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 15 Jun 2026 23:15:37 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 15 Jun 2026 23:15:37 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:15:37 GMT
WORKDIR /usr/share/logstash
# Mon, 15 Jun 2026 23:15:37 GMT
USER 1000
# Mon, 15 Jun 2026 23:15:37 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 15 Jun 2026 23:15:37 GMT
LABEL org.label-schema.build-date=2026-05-23T16:23:32+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-23T16:23:32+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 15 Jun 2026 23:15:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53f95b2aa14a1f02505779ade1fc65c323dd9bb64199a40ffe282c1dcbc874`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 4.8 MB (4775138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305658049786001c05c67f784827f6c760e0ac87046a122e89b7e50427e82483`  
		Last Modified: Mon, 15 Jun 2026 23:16:22 GMT  
		Size: 472.3 MB (472279138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37daf38c424228f8e72c0afb7ef1f7801506b5a0089252a843116ca505509dc`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9551304999005cb7e9c71ac5905705e680878f994356a60102c11f845ebec902`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcec66ae37327a73b17e92b2c60c220157e07fd00ce2cd1c1ae9ab90d128b113`  
		Last Modified: Mon, 15 Jun 2026 23:16:15 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fa51eba61f1d37e177c950f471697e8011afefd2ee5d52443a591ecaff0a10`  
		Last Modified: Mon, 15 Jun 2026 23:16:15 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d51a8bf2a89eb0d7d3dcd50722a7b1559cb3536ba6eb512ae555412971359e`  
		Last Modified: Mon, 15 Jun 2026 23:16:15 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f16a056f997b9dec3be4974aab879508bd7c19ce26a7949db45d0a3e0b7ac7`  
		Last Modified: Mon, 15 Jun 2026 23:16:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e43d48dbb9bbbb842bccde184c54686a60d8f0e2f4c5d89f1c56a0fb90fe3`  
		Last Modified: Mon, 15 Jun 2026 23:16:16 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.5` - unknown; unknown

```console
$ docker pull logstash@sha256:6b72893ba2a15af65c1c66850d992d57774021e989eefea7ceb46e56ab7660b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbf4e852ca841b7f409ad0d16c2f8051f56bb07b164b56b49a0ab89531220d3`

```dockerfile
```

-	Layers:
	-	`sha256:3886e89ce3ed4bc5bebe7a3c35df8e4c6bfdd0ddae7abc263bea7059159f3926`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 2.1 MB (2111899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dedb7ac10b8cf56eca8a93bf134aa6dfd920bd07a1c8e06b0d338566ba18f15`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:28573b107910de54abbfc4d8f916c5715b187645783982d1386b3e000800f11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.5 MB (514483852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18825047aa0e8c46f7ac2f2d272aaa9839b0f1dd2ee3ad350840e2767a829542`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:14:27 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:14:27 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:27 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:14:27 GMT
WORKDIR /usr/share
# Mon, 15 Jun 2026 23:14:29 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:15:20 GMT
WORKDIR /usr/share/logstash
# Mon, 15 Jun 2026 23:15:20 GMT
USER 1000
# Mon, 15 Jun 2026 23:15:20 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 15 Jun 2026 23:15:20 GMT
LABEL org.label-schema.build-date=2026-05-23T16:23:32+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-23T16:23:32+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 15 Jun 2026 23:15:20 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6592ed4ae7acd696ddf2a6fdd60c662702632b5d34653350dc67177666086`  
		Last Modified: Mon, 15 Jun 2026 23:15:58 GMT  
		Size: 4.8 MB (4769247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca1e7fdb53e288ca813caaf598ca1dd625ecbd6ce1b9c8fb1c7865a203f0cb4`  
		Last Modified: Mon, 15 Jun 2026 23:16:05 GMT  
		Size: 470.6 MB (470576849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84e6f09852fde9d6840baa30a1d19baf0629183228c7fc049e6b5deb626f812`  
		Last Modified: Mon, 15 Jun 2026 23:15:58 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d47400428c542c4da41d6ab0f62cc17f2f2376487ffc6a35d1c16e230b5004`  
		Last Modified: Mon, 15 Jun 2026 23:15:58 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7da3a81114e213321b455f7881072ef325f6ba07a0b06eb6bcba468192909f3`  
		Last Modified: Mon, 15 Jun 2026 23:15:59 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa19199934d5fbc369b7f6c38690cac6f4c71eab07cc39552146aab125a47b`  
		Last Modified: Mon, 15 Jun 2026 23:15:59 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2233774042bca1fcb38da6864a8859a17ca2a0061d59be34d0546bd0dba96937`  
		Last Modified: Mon, 15 Jun 2026 23:15:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf56acb6965881b4271f877a906bb8b3f71bdaef6612aaba886f8765e4c0095d`  
		Last Modified: Mon, 15 Jun 2026 23:16:00 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb6c7787e2eaae23e0069bb60de264a5b0a01ef310a0b46e40bab09a10e6487`  
		Last Modified: Mon, 15 Jun 2026 23:16:00 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.5` - unknown; unknown

```console
$ docker pull logstash@sha256:96c69a41eebb7247f874d91ee1ca72bde8075387a3dd700af0a87af3b6c455ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d19936fc9ff7820840c7c18852c8a53ab28803f7053ed1f19981caa9c7b0fb`

```dockerfile
```

-	Layers:
	-	`sha256:f8bbe01dca4cb0bd3643d8e1ad944414dc0f1155d8666c127d7eddb8563451fb`  
		Last Modified: Mon, 15 Jun 2026 23:15:58 GMT  
		Size: 2.1 MB (2112469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab38340696ab804f58112b196aed58486d1888cd9827ed59722739c95a57968b`  
		Last Modified: Mon, 15 Jun 2026 23:15:58 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.2`

```console
$ docker pull logstash@sha256:648a781b7360736754a9f583f7819d166be9dcee42d272bbce7d67278f529398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.2` - linux; amd64

```console
$ docker pull logstash@sha256:757cbff166ca2e68887ca89c60ff8082c1f6fcfa920efb80db931c8a51a0ea8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.4 MB (524435028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f798eb45116e783bac26177364cf2f39d48492075d1e0c45053d160e0e68a2a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:15:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:15:10 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:15:10 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:15:10 GMT
WORKDIR /usr/share
# Mon, 15 Jun 2026 23:15:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:16:04 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:16:05 GMT
WORKDIR /usr/share/logstash
# Mon, 15 Jun 2026 23:16:05 GMT
USER 1000
# Mon, 15 Jun 2026 23:16:05 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 15 Jun 2026 23:16:05 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 15 Jun 2026 23:16:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6d3afa2da55aebe1433c4e560b1e3190d53420e1185a6fb24dbd147ced548e`  
		Last Modified: Mon, 15 Jun 2026 23:16:42 GMT  
		Size: 4.8 MB (4775109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4eefa873493c008faa123f0343a5d298310c0c0e3c5e01f8a9b531867594db`  
		Last Modified: Mon, 15 Jun 2026 23:16:54 GMT  
		Size: 478.7 MB (478714901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5bdb6058a800ae9b083ef950ebacd167dff4b3817d774634d039bd96554b8b`  
		Last Modified: Mon, 15 Jun 2026 23:16:41 GMT  
		Size: 6.4 KB (6367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0993c936a52c2113b66d15fcba049cb80e5c26785a5133a2bc5132935d453470`  
		Last Modified: Mon, 15 Jun 2026 23:16:42 GMT  
		Size: 255.2 KB (255191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0105efd551d3f43e5655b08921d0eb2df2a4339ab7f0662046061b15ee00feb3`  
		Last Modified: Mon, 15 Jun 2026 23:16:43 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f118e4f4a5f36a0743ddb3aab006d0044ec1a4912851728acd871d899e64e430`  
		Last Modified: Mon, 15 Jun 2026 23:16:43 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f330cca4c8365005afebf7e87e762b34871dbd9a5f918534f9844fb13f001ed`  
		Last Modified: Mon, 15 Jun 2026 23:16:43 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd9368e0d0772fa36a4d43240280333213eeab0acf21dfeb03ebbef67ddb0fe`  
		Last Modified: Mon, 15 Jun 2026 23:16:44 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7178dda110a6f8dc24e7178ba8e6b2f81e3ae508f363b6170520c4cc6f042d`  
		Last Modified: Mon, 15 Jun 2026 23:16:44 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:b45c2106aad26bb65843cce45404dad7e01def23323bf9c9b9b3391cacbd1cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e58da10d20376f80c9454e4e7a6687bebd427057ed370050455428b18f82f5`

```dockerfile
```

-	Layers:
	-	`sha256:9a3d51a453084c5a61de746fdaac073e266aaf600f3390a1de397a77ce47bc7d`  
		Last Modified: Mon, 15 Jun 2026 23:16:41 GMT  
		Size: 2.1 MB (2117897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e790a31c51dc1f75ac8058bf18d00bf95060534558a7f27b58b29cd36f62fc2`  
		Last Modified: Mon, 15 Jun 2026 23:16:41 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:12fa0622b470f87267310eb3881f543336d19daead5bae58047f2c71001c89ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520917841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0145bd4e28433030a02f4196340b2774aadde8c73810e27597dea87bd1f0c90`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:14:31 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:14:31 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:31 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Mon, 15 Jun 2026 23:14:31 GMT
WORKDIR /usr/share
# Mon, 15 Jun 2026 23:14:33 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
WORKDIR /usr/share/logstash
# Mon, 15 Jun 2026 23:15:31 GMT
USER 1000
# Mon, 15 Jun 2026 23:15:31 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 15 Jun 2026 23:15:31 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Mon, 15 Jun 2026 23:15:31 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fd8f1e7ce7cbb741ef49b9bc9fdb148993453ba881f04614af92f5e83a59fb`  
		Last Modified: Mon, 15 Jun 2026 23:16:11 GMT  
		Size: 4.8 MB (4769159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32581674843d054565b7213a821949a4df2e0493cd4dba407b50ec832b96136c`  
		Last Modified: Mon, 15 Jun 2026 23:16:21 GMT  
		Size: 477.0 MB (477010847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cac5f5f25088452c06d856becd206d110cb7e3cfce691211a051e24eb51cb7`  
		Last Modified: Mon, 15 Jun 2026 23:16:10 GMT  
		Size: 6.4 KB (6364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e67b1ff21af1237c58dcce1649a1d960ba49fcceb9224be5b4dc515425d58a`  
		Last Modified: Mon, 15 Jun 2026 23:16:11 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebe8542a67266909d942641983fa45bc1deb5ef5a203473adddfbdbee9f7097`  
		Last Modified: Mon, 15 Jun 2026 23:16:12 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e8a22dd39224a492ca9357a3caa10522c06f5fecc42dfbb2301f591fed0f4e`  
		Last Modified: Mon, 15 Jun 2026 23:16:12 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74425dc94b44c678381611bdcc27be0990636d5bd2dc2e88781d581d06273f00`  
		Last Modified: Mon, 15 Jun 2026 23:16:12 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529fc3d3e0abadc067571d95bac95534c17bee2174468cb8fd27d3c9cba8389a`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d66d2c19d56b7b71e1ab014ddff9f424b3afb8573de330e74d57607746a85`  
		Last Modified: Mon, 15 Jun 2026 23:16:13 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:7b060c670a0d88ff0e8656529f4891ed49fa92f504b67ee8fcfd19331901d228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c045d60409e09b3fd414a541ae035e68142421a65cc63a71ad2d470a25e2324`

```dockerfile
```

-	Layers:
	-	`sha256:22838af172254b3fec2e43209e78ff20358dd37cc698fef9f4b3fee66a72f932`  
		Last Modified: Mon, 15 Jun 2026 23:16:11 GMT  
		Size: 2.1 MB (2118467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9139f2547203d2600d2eb07717c6a3d59f481af0b808ff61d46cb2054646df`  
		Last Modified: Mon, 15 Jun 2026 23:16:10 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
