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
$ docker pull logstash@sha256:db725eac73f128a0cce7605bd2f6e5f4357b43a7236227638e681795f9b25c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.5` - linux; amd64

```console
$ docker pull logstash@sha256:f5914241254324c489c89e511721bfcfcd3d02c56082558a1cedb6f04d6a8d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.0 MB (518006255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad86fca152a7a38e22b0c5f606fc582f9fd5722f2612c0ff4088c2532fbae6a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:45:15 GMT
ENV container oci
# Tue, 02 Jun 2026 05:45:16 GMT
COPY dir:089626db9f0e556d2460ea9b02a44cc63366766c2d8912a1fd05fdd542cbb8e4 in /      
# Tue, 02 Jun 2026 05:45:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:45:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:44:58Z" "org.opencontainers.image.created"="2026-06-02T05:44:58Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:44:58Z
# Tue, 02 Jun 2026 22:46:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:46:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:46:18 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 22:46:18 GMT
WORKDIR /usr/share
# Tue, 02 Jun 2026 22:46:20 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:47:09 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Jun 2026 22:47:09 GMT
USER 1000
# Tue, 02 Jun 2026 22:47:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Jun 2026 22:47:09 GMT
LABEL org.label-schema.build-date=2026-05-23T16:23:32+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-23T16:23:32+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Jun 2026 22:47:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf97a6554785265d30af77ef9ad9c114835e29b71becaab3803fa6e27dbaa6`  
		Last Modified: Tue, 02 Jun 2026 22:47:46 GMT  
		Size: 4.8 MB (4775301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2b450474e6c23e5a0f2be449301a0d8b7da98aa0fb4bd309030622e632a04a`  
		Last Modified: Tue, 02 Jun 2026 22:47:55 GMT  
		Size: 472.3 MB (472279172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187bbd6e7f59321a2c0cc61746efe444bcff988705f1cbf3206f131358a5836d`  
		Last Modified: Tue, 02 Jun 2026 22:47:46 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07562b5a5a40bfb4047d9f536fec04d8a11e3046764cb8f89cde84baf73e7a`  
		Last Modified: Tue, 02 Jun 2026 22:47:46 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790d6aece595d26ecef34bd030d4a5ebfb299cd01e5288274fe2596cefecb70`  
		Last Modified: Tue, 02 Jun 2026 22:47:47 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f30e49e2486746e75c927cdc64ff947880c4711164e360728acda4f854b6bc`  
		Last Modified: Tue, 02 Jun 2026 22:47:47 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d51aab2321b2f35f5ec4d7efaa5279856f9cf0ae96592b0f33502d34067f84`  
		Last Modified: Tue, 02 Jun 2026 22:47:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f783664505f44f11647ff8dc211cdd3c85d37210caab77ebf491485ad42f2663`  
		Last Modified: Tue, 02 Jun 2026 22:47:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67110423795d38d0a5645e0b21595d37e161801d93d343f23b2eb3b10443cabd`  
		Last Modified: Tue, 02 Jun 2026 22:47:48 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.5` - unknown; unknown

```console
$ docker pull logstash@sha256:b71b4d9b0a740ff9595fd9e29b6648ff8d0e2f9704b607cc66d0140460f789d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1083ad8440fe36e57f8631b17322dc2222ac519120a36ba7d1fed37eb5246c99`

```dockerfile
```

-	Layers:
	-	`sha256:9200e3f955c11f386d4ae1bf6d80a89f172cf3d0eba99fada7b8652c85939305`  
		Last Modified: Tue, 02 Jun 2026 22:47:46 GMT  
		Size: 2.1 MB (2111895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad5d43d0c51b231d6f48cb09582744d17fd4fbda1a4937bb3027ef89f493e555`  
		Last Modified: Tue, 02 Jun 2026 22:47:46 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:a68497e09a10ecc6e443622ab2058c244cb39a4ba7858e90de8672d35f7696fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.5 MB (514475637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e59c34d780b7571bcb69584a6024318eb651fd37d037429327da6258e014c9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:50 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:51 GMT
COPY dir:45e3b0db7c7574b63ad7ec3e8aa88c1c154d382f5d855d74a5a8b46ed379a850 in /      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:51 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:37Z" "org.opencontainers.image.created"="2026-06-02T05:43:37Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:37Z
# Tue, 02 Jun 2026 22:45:41 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:45:41 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:41 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 22:45:41 GMT
WORKDIR /usr/share
# Tue, 02 Jun 2026 22:45:43 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:46:31 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Jun 2026 22:46:31 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 02 Jun 2026 22:46:32 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 02 Jun 2026 22:46:32 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Jun 2026 22:46:32 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Jun 2026 22:46:32 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Jun 2026 22:46:32 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Jun 2026 22:46:32 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:46:32 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Jun 2026 22:46:32 GMT
USER 1000
# Tue, 02 Jun 2026 22:46:32 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Jun 2026 22:46:32 GMT
LABEL org.label-schema.build-date=2026-05-23T16:23:32+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-23T16:23:32+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Jun 2026 22:46:32 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5af23a825c7f33f0578296ca19c2b88e3b68d56479c6280d0d7adefe94a116`  
		Last Modified: Tue, 02 Jun 2026 22:47:09 GMT  
		Size: 4.8 MB (4770382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61136f9b6d820388f770c193b49c215c3b425de654640538cf8fa1fc5f3e3059`  
		Last Modified: Tue, 02 Jun 2026 22:47:21 GMT  
		Size: 470.6 MB (470577345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b5c05255a76d5f95e9086049ee45d0a91de8b4877f5c8f02a93f553a8bb855`  
		Last Modified: Tue, 02 Jun 2026 22:47:09 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688e76a00cdb8c1108996a6866fb8d231648e7bd162efdacfa72af3eadc315d7`  
		Last Modified: Tue, 02 Jun 2026 22:47:09 GMT  
		Size: 255.2 KB (255187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fbf466928f36b0acd429a593963575505042a011c6124da87d694ba8b5fb0c`  
		Last Modified: Tue, 02 Jun 2026 22:47:10 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca6e45704f035f881d25a623aee14476812051ec34be2b27381c85500790f6b`  
		Last Modified: Tue, 02 Jun 2026 22:47:11 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdf2f415dbcfec28f102234cbcb6177586e8dbe820681062d2b830f8918d8d8`  
		Last Modified: Tue, 02 Jun 2026 22:47:11 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeeaa112fb302af041af64e04bf2bbf759cdf447fb678ce37fa567fb2404989`  
		Last Modified: Tue, 02 Jun 2026 22:47:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eecc872bd608fe61492e0c2c4858cbc98d2fa7deb123ba1ac0e2317ee415c8a`  
		Last Modified: Tue, 02 Jun 2026 22:47:12 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.5` - unknown; unknown

```console
$ docker pull logstash@sha256:37ccec461a489f8f77ed83212ad19d7ae8b5a261195bde17ed57e6a8475b3e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee631871011908db3d82f3f8059f0084b84fe306e36a24c4eca7d219411b78d`

```dockerfile
```

-	Layers:
	-	`sha256:269df29d47c310834323bd3f7ff6c63e426b1166e92b1e9a452457d6617aa198`  
		Last Modified: Tue, 02 Jun 2026 22:47:09 GMT  
		Size: 2.1 MB (2112465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28114dd00469418b5cc070f863588b56093c3fb8f1b963d94a3f11238effbf97`  
		Last Modified: Tue, 02 Jun 2026 22:47:09 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.2`

```console
$ docker pull logstash@sha256:37bba85d7c27ae42a429a77812ae33d493928ebee175de74bc1d6ba9a26e53b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.2` - linux; amd64

```console
$ docker pull logstash@sha256:10ecfbbf994d0ec9039937fc8bfac3e5851a5e74d3b275812a551cc2354722a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.4 MB (524441979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e9d7bb77e135244c9f445b8de1207726d28e0af8d91cc17b8f68979834d296`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:45:15 GMT
ENV container oci
# Tue, 02 Jun 2026 05:45:16 GMT
COPY dir:089626db9f0e556d2460ea9b02a44cc63366766c2d8912a1fd05fdd542cbb8e4 in /      
# Tue, 02 Jun 2026 05:45:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:45:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:44:58Z" "org.opencontainers.image.created"="2026-06-02T05:44:58Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:44:58Z
# Tue, 02 Jun 2026 22:46:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:46:18 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:46:18 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 22:46:18 GMT
WORKDIR /usr/share
# Tue, 02 Jun 2026 22:46:20 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:47:10 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Jun 2026 22:47:10 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 02 Jun 2026 22:47:10 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 02 Jun 2026 22:47:10 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Jun 2026 22:47:10 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Jun 2026 22:47:11 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Jun 2026 22:47:11 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Jun 2026 22:47:11 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:47:11 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Jun 2026 22:47:11 GMT
USER 1000
# Tue, 02 Jun 2026 22:47:11 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Jun 2026 22:47:11 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Jun 2026 22:47:11 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a81640e47e9f1e3d06bcb492062889c21b1b8c13bee030a777af6bc524e703a`  
		Last Modified: Tue, 02 Jun 2026 22:47:48 GMT  
		Size: 4.8 MB (4775309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43335dc07fe133b94268c7aae98d661554dee5998c530cbb4025d08f2acc1e06`  
		Last Modified: Tue, 02 Jun 2026 22:47:57 GMT  
		Size: 478.7 MB (478714811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fd0ec17aae1eb5ab74758ed7d198ba41e901dd7be1453fe0daa153d28eebd5`  
		Last Modified: Tue, 02 Jun 2026 22:47:48 GMT  
		Size: 6.4 KB (6367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db3c7c0f4464f12def70a29b521d5b5fa4ba706570a20546a3b9cc72b0c5380`  
		Last Modified: Tue, 02 Jun 2026 22:47:48 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916811c617eb7653cf085f0959660a96c660674dfcd9b0f13fa0f49d33b37c82`  
		Last Modified: Tue, 02 Jun 2026 22:47:50 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f508167c1cf503d04c14b7c3bf54f0aef9f4a13ea2f22bacc7447ee34e42a22c`  
		Last Modified: Tue, 02 Jun 2026 22:47:50 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e788b34548cd8d94f5a0a15bd042ae0afe93133ac80f010619e0ba3f97882e3f`  
		Last Modified: Tue, 02 Jun 2026 22:47:50 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6d1d64c7f3009798ff3c1dcddcb0db148b1ea53f8ac9514e8e30003015e7f`  
		Last Modified: Tue, 02 Jun 2026 22:47:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc776fa85980ab06499305863ad6b6ab95dea5b49edfb82a65c4d300432a7ca2`  
		Last Modified: Tue, 02 Jun 2026 22:47:51 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:cbb103bfb4bae4b462b2274c873aaa4f9be4d2848789fcb073992acab7d6ae8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c567de7d602ed2c633e00aa853b7b9da7dcd15acccd549abc3166efd9f39cd11`

```dockerfile
```

-	Layers:
	-	`sha256:974b7f9cfecd4385adb5e936dd5ff1f0fc5f43d7a8d5ebc7703c21059ec57725`  
		Last Modified: Tue, 02 Jun 2026 22:47:48 GMT  
		Size: 2.1 MB (2117893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b946fd7e7d69b11f76d7b0a5744b9032922586328bae84ca1769b15d975a660`  
		Last Modified: Tue, 02 Jun 2026 22:47:48 GMT  
		Size: 30.2 KB (30199 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:5ca83d16deb9f56d7ec53b0e8a6889f74ebf6a18896e02fd563eb4040b753db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520908798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9fe5920e9cc92792db869dff6957a297a55e542e7192003f2779e471fe776f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:50 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:51 GMT
COPY dir:45e3b0db7c7574b63ad7ec3e8aa88c1c154d382f5d855d74a5a8b46ed379a850 in /      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:51 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:37Z" "org.opencontainers.image.created"="2026-06-02T05:43:37Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:37Z
# Tue, 02 Jun 2026 22:45:42 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:45:42 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:42 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Jun 2026 22:45:42 GMT
WORKDIR /usr/share
# Tue, 02 Jun 2026 22:45:44 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Jun 2026 22:46:37 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Jun 2026 22:46:37 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:46:37 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Jun 2026 22:46:37 GMT
USER 1000
# Tue, 02 Jun 2026 22:46:37 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Jun 2026 22:46:37 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Jun 2026 22:46:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3c44ab2e4e391cadafbd26ebc8cab451b2ac11b9af71efb639469f1a5162cb`  
		Last Modified: Tue, 02 Jun 2026 22:47:17 GMT  
		Size: 4.8 MB (4770328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13481fda6d71e7e2f9a70c9f88d45266df155c0b89ac87aa7fef6283f1a1f7c4`  
		Last Modified: Tue, 02 Jun 2026 22:47:26 GMT  
		Size: 477.0 MB (477010498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa673dfa2dac2ab9394c8ba3c1f26ff74d5148da344754ea5fadad73bc1ab089`  
		Last Modified: Tue, 02 Jun 2026 22:47:16 GMT  
		Size: 6.4 KB (6367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c91494448c183f365e81a4a4c87c078e10890b329359a28eb367f0cd774ba2`  
		Last Modified: Tue, 02 Jun 2026 22:47:16 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb94aab9e9fd0093046e4e9c80bc32805e8e109d5b7341ba0b7e1ffe038074e7`  
		Last Modified: Tue, 02 Jun 2026 22:47:18 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c1cebcac582209bac8e0939a24c99a9a4935bf293a32266f564292352c0cc1`  
		Last Modified: Tue, 02 Jun 2026 22:47:18 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabedf780b66275a763a6ecd1856c1d6a214d0b2c6b2a23d40f1b0559d09970c`  
		Last Modified: Tue, 02 Jun 2026 22:47:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2adc95fa1edecae8e9881b400c2db9da376ae7d6ea7f2a378f95ca9acc982e`  
		Last Modified: Tue, 02 Jun 2026 22:47:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e4fe5a92ad038c0d1a7f949e365bd6482a2f0a8a9126962aa4c56922ce7e8`  
		Last Modified: Tue, 02 Jun 2026 22:47:19 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:205eb01151c945d6e52b0e5dbf2ab28b211eb8e96128b663420936bf467357e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d467e7759941f0c3fcd90cb4ba93f1a8ddddcb6d4356a185a566a718e1fcf9`

```dockerfile
```

-	Layers:
	-	`sha256:9c62c9fc42e8bd0d1f82ee01de1f4d0e792b6cd2adb9b7c12cf85d9b53a2e6d7`  
		Last Modified: Tue, 02 Jun 2026 22:47:16 GMT  
		Size: 2.1 MB (2118463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:205fb5e1a03a4883236b9d9c5bb1ad00065b14e897eb5890d3cbb1ea69da3aee`  
		Last Modified: Tue, 02 Jun 2026 22:47:16 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
