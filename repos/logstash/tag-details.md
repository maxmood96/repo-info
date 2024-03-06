<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.18`](#logstash71718)
-	[`logstash:8.12.2`](#logstash8122)

## `logstash:7.17.18`

```console
$ docker pull logstash@sha256:1680b94bcdb2b1dd5818d54b51835cd8e083158c5dd033862ae4ba06b280daaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.18` - linux; amd64

```console
$ docker pull logstash@sha256:75b9ed2a6dd0829fb5c13c6164f7b2eaf95a9495bd9ce701baddcc6880286393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.3 MB (443254266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16183b947ee608e34ccf2183ea627fa784c2f26b855a0e8c0f7f9df7e9902ad5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 06 Feb 2024 11:29:54 GMT
ARG RELEASE
# Tue, 06 Feb 2024 11:29:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 06 Feb 2024 11:29:54 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.18-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.18 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/logstash
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 06 Feb 2024 11:29:54 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
USER 1000
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.18 org.opencontainers.image.version=7.17.18 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-23T20:45:18+00:00 org.opencontainers.image.created=2024-01-23T20:45:18+00:00
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8186857aa53cb7b2ce9078a89c299a124c3cf46a85a6d601a8b0e625e860865`  
		Last Modified: Wed, 06 Mar 2024 02:56:53 GMT  
		Size: 47.0 MB (47030076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8020c935b4b753b7cb3489aae73e17aff138ecd896135a53abaf2af3255e1fa3`  
		Last Modified: Wed, 06 Mar 2024 02:56:52 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480c3db6a1795f23ffe55705603480ba5bcf5820fb62e50d30f1878299e66b13`  
		Last Modified: Wed, 06 Mar 2024 02:56:58 GMT  
		Size: 366.9 MB (366860382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a704b979f3516590ded619ec33632e11f293731f862ce1d4c5145c7c91b7d8b0`  
		Last Modified: Wed, 06 Mar 2024 02:56:52 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7152df9aaf52046046fc74b778862b7e0d4959bcb7f13ce803b271877d8fa`  
		Last Modified: Wed, 06 Mar 2024 02:56:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff214ea693306f25fdbd91d28b487d6fcb5978feddada9e785012501f44c18`  
		Last Modified: Wed, 06 Mar 2024 02:56:53 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45934522dd1d78ecb2778acc16db6294f35dd116fe44726a36a346a748e4f292`  
		Last Modified: Wed, 06 Mar 2024 02:56:54 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33261515fd4a40fa008967c7c9eee8b1beaaf84fa3e7f97d4c2972d810ee82c`  
		Last Modified: Wed, 06 Mar 2024 02:56:54 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d312e78921d1abb8342176707ff9f1971fcb02dc0ebe9c8ff7492f27f7144981`  
		Last Modified: Wed, 06 Mar 2024 02:56:55 GMT  
		Size: 1.8 MB (1844905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d8d88d5abba5860199e4444c8546dc99709f053747540cb2d9847fcf58ba96`  
		Last Modified: Wed, 06 Mar 2024 02:56:55 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.18` - unknown; unknown

```console
$ docker pull logstash@sha256:83c499dd458892fc1f4f1cca81e2be5e1131c3335f4812eebf491c24aa34f7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3271321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513f6cbe485e0ef45e440fb90bd7874bdc721afbe67255da387f1784df00c1eb`

```dockerfile
```

-	Layers:
	-	`sha256:432a4e2b0a83ddd2c3c417e700e2adb5f91f6f326b233dbd669d2a64dd8cda50`  
		Last Modified: Wed, 06 Mar 2024 02:56:52 GMT  
		Size: 3.2 MB (3239152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828bf20c9e0faed218ea7588d7bf516f266b08e577b5e8bbd5a723a626cbd1d8`  
		Last Modified: Wed, 06 Mar 2024 02:56:51 GMT  
		Size: 32.2 KB (32169 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.18` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:dc27e4572bbdf3e784fca668c6f6260d1a0ad9c8f36bd4b031702ebdadd0a207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.3 MB (428293635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6455a8057dfeabda3dedeacf4b30071c7f135f8df888d0c2d68c021e98299126`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.18-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.18 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/logstash
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 06 Feb 2024 11:29:54 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
USER 1000
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.18 org.opencontainers.image.version=7.17.18 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-01-23T20:45:18+00:00 org.opencontainers.image.created=2024-01-23T20:45:18+00:00
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ef344003285a8f726a4249086f99744ed568b8652c21ee2a064bf4855d270`  
		Last Modified: Sat, 03 Feb 2024 07:56:10 GMT  
		Size: 36.9 MB (36873983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf161b4dc6d8800719d55037270976fa1608433889c52cb37c39fd963c86df5`  
		Last Modified: Sat, 03 Feb 2024 07:56:09 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfa0cea1fc79ad0cdc55745f2504e8596e34620a1610d1235a241a2c9e9ae45`  
		Last Modified: Tue, 06 Feb 2024 22:47:04 GMT  
		Size: 363.6 MB (363594542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016e55ad66bb0dcdf060c1eefa31209ffb0ed1eb76e1dd87cc94a2cda9e362f6`  
		Last Modified: Tue, 06 Feb 2024 22:46:57 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935aeac8eb6c7ed627705b36d83c758974fb4bedc75dac0a591e0148ec7cb130`  
		Last Modified: Tue, 06 Feb 2024 22:46:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11176d2749a7befedf6f424f7ee0085110bfab4b4467a943792aec80b957c748`  
		Last Modified: Tue, 06 Feb 2024 22:46:58 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4c6cac6128f56aa03af6edadb5682dd2e192fba54394bf14b5e95b51e73e94`  
		Last Modified: Tue, 06 Feb 2024 22:46:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14443f2b8850101173f46c130dc2f7d64f7807130a5d29bb2cf27f1b3423419`  
		Last Modified: Tue, 06 Feb 2024 22:46:59 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99a32fb0d22eb80d252f383873bc913ea2de97ffad6174cd13584ea37cf773f`  
		Last Modified: Tue, 06 Feb 2024 22:46:59 GMT  
		Size: 1.8 MB (1844905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d08b05db94104361a5d8f8992b910e10a09c2251fa48cb2366b05905a2e9a6a`  
		Last Modified: Tue, 06 Feb 2024 22:46:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.18` - unknown; unknown

```console
$ docker pull logstash@sha256:396c2459c940fdd47a892875a4f1f03a7ff71db2bc10f00cff2e2d979db2511d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2971062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429a15760994c91c9c79dbaeb3b64673aa17f83911c6c5ddda23dc798ddb3ccc`

```dockerfile
```

-	Layers:
	-	`sha256:c77a87a1816c5a3daa5491c1ee91c10b42d2ac676ff470eea796f3c25e0e3a07`  
		Last Modified: Tue, 06 Feb 2024 22:46:58 GMT  
		Size: 2.9 MB (2939050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e6313766521760a5cc635a5b323fe43f23d3a8c09e891867c2db81e5a675fd`  
		Last Modified: Tue, 06 Feb 2024 22:46:57 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.12.2`

```console
$ docker pull logstash@sha256:e1820d2b3d44b5b1de331d18250b02eeae4678867cdd8dbf927b4329b1bfc8a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.12.2` - linux; amd64

```console
$ docker pull logstash@sha256:a15a827088a01c634bb4efe6676f3b5b9f2c8dd50728c56512d61e5cd145b8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.5 MB (426473321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431435ffc548307a5c05c898379c755985b508f5df8a75539704b3fd9c32877b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 12:50:52 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.12.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.12.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/logstash
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 22 Feb 2024 12:50:52 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.12.2 org.opencontainers.image.version=8.12.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-02-16T16:21:40+00:00 org.opencontainers.image.created=2024-02-16T16:21:40+00:00
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06487f034a6ce33e0209d9e4156742f8830caf4f433370cc6fecf70c75c3cc23`  
		Last Modified: Wed, 06 Mar 2024 02:56:39 GMT  
		Size: 47.0 MB (47030137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c43214d2b3d3d7620ceaa7299ae59168d342cf53fade7caaf35ce522e54962`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0083a2fffe6a3a65783a62652630f398c25c04743caa28b89f62f027d9f42a5`  
		Last Modified: Wed, 06 Mar 2024 02:56:44 GMT  
		Size: 350.0 MB (350017662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713c8daee1d77439f3909fe390f39cd1bb42906441c3011364764d868981d800`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f089b9a3e2a4dbfa337aebf874d8e11a33f2d692d342faca9b4c97079e62be6`  
		Last Modified: Wed, 06 Mar 2024 02:56:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763ed5b971ff4dd54cf834e5d211ac11635c1ad12f18891251663831c95be5d9`  
		Last Modified: Wed, 06 Mar 2024 02:56:39 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de2b6f9e65f2e298ec60c209ed9b539fee80d393c5cb298ecfb2febece47dbb`  
		Last Modified: Wed, 06 Mar 2024 02:56:40 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3779bf305ab938f068cd6e982e03f9c1996594f28ee7dcd877f74b369d59f54a`  
		Last Modified: Wed, 06 Mar 2024 02:56:40 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329ac120e52abb6b2409a116fb071ece0e6a771f5ce1bcaff8888ba724d1ad87`  
		Last Modified: Wed, 06 Mar 2024 02:56:40 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ad5f6d6626aa280bc6895f88216d150e1da176bae728c637075edbaf41e1e9`  
		Last Modified: Wed, 06 Mar 2024 02:56:41 GMT  
		Size: 1.9 MB (1904103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b89468fac553ad6c9adad8d0a39af0df82f1fd2963d1cf5fbe1e1bbd77961a`  
		Last Modified: Wed, 06 Mar 2024 02:56:41 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.12.2` - unknown; unknown

```console
$ docker pull logstash@sha256:f12252962e9e68041e1488ab0ec8ba6177bb4bd2d54da70df89fe441927dc888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a2e40a4c91d726c774000563fba09272fea20f12d8088f82c000b85157829d`

```dockerfile
```

-	Layers:
	-	`sha256:079019ef62a7af2cc1fc8b76e177742c43add1ea80417ef9a78fed2fab6099e7`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 3.3 MB (3325957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c9334ce379f5d5689e86e42067f8fbef746918131d33c4ed30371ec1613b75`  
		Last Modified: Wed, 06 Mar 2024 02:56:38 GMT  
		Size: 34.7 KB (34698 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.12.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f4c6ea2f0823c4fb2e635b429283f212d19b9fd6677a10022403ba8635fd5bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413599609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602a85f0b19983db3bc9952acb6525c4785b502f970e3207baa827a4e8c7976e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 12:50:52 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.12.2-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.12.2 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/logstash
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 22 Feb 2024 12:50:52 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.12.2 org.opencontainers.image.version=8.12.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-02-16T16:21:40+00:00 org.opencontainers.image.created=2024-02-16T16:21:40+00:00
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ef344003285a8f726a4249086f99744ed568b8652c21ee2a064bf4855d270`  
		Last Modified: Sat, 03 Feb 2024 07:56:10 GMT  
		Size: 36.9 MB (36873983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf161b4dc6d8800719d55037270976fa1608433889c52cb37c39fd963c86df5`  
		Last Modified: Sat, 03 Feb 2024 07:56:09 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f950ae0418a3e60f3c2c64201f381fbe3a1e5c685500bc414407055401cec1`  
		Last Modified: Thu, 22 Feb 2024 23:59:01 GMT  
		Size: 348.8 MB (348838807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24c3bc26c5a2191f4e34142f8435d3696e7a9249dd2eada6106e08a9f3291fb`  
		Last Modified: Thu, 22 Feb 2024 23:58:53 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ad8ad5582d9f9f716cbe39c49eb1249e3936b9b4c69d65cbaa82138e09e16`  
		Last Modified: Thu, 22 Feb 2024 23:58:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51132973bcef7bd14167e6c7a4de950a292860f2e944a8dc6256d84dd9daaaa3`  
		Last Modified: Thu, 22 Feb 2024 23:58:53 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d34a0ba25ae125f062eeca5a8cf6999133ccbcfd6dc8dd1a8e587b35bc61e3`  
		Last Modified: Thu, 22 Feb 2024 23:58:54 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e1268d2d8aa92eb6ef9a84bf9904273eafd02a7c113be432014589a4fa2b68`  
		Last Modified: Thu, 22 Feb 2024 23:58:54 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8604386e74f5edfef9b699a34d5a46af0119c838183effcd4387834930ff6597`  
		Last Modified: Thu, 22 Feb 2024 23:58:54 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7768073088812b9003ff1ae8b759f73ca8ed14efb8b62fb7c356a21c6f229493`  
		Last Modified: Thu, 22 Feb 2024 23:58:55 GMT  
		Size: 1.9 MB (1904105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0903f97c04ca488ce06bbeca2b47983cf937c7cd02db1a1ea4f4d09d3b02b0`  
		Last Modified: Thu, 22 Feb 2024 23:58:55 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.12.2` - unknown; unknown

```console
$ docker pull logstash@sha256:18036b2c9123c7f36f402130b5ea6f0a9d392d33c6c89167292c8c803ee466bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3360719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f9dc989bc03b4283cfd925b9a77cca93307af82e9c0d7086a7fe55d81740c4`

```dockerfile
```

-	Layers:
	-	`sha256:4eae76deb07857ccf4d97bb22be73b370ef91881907081ea18d8b7ebf50fc19a`  
		Last Modified: Thu, 22 Feb 2024 23:58:53 GMT  
		Size: 3.3 MB (3326177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a3c461e978a6fbf621677cf98c0b44c629f5c8da7d9efd221e48ab0c84377e`  
		Last Modified: Thu, 22 Feb 2024 23:58:53 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json
