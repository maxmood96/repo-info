<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.18`](#logstash71718)
-	[`logstash:8.12.2`](#logstash8122)

## `logstash:7.17.18`

```console
$ docker pull logstash@sha256:73ae89056492ffc9dcb03aef412d7ccc8f4525766e226aa4a004416314ea4326
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.18` - linux; amd64

```console
$ docker pull logstash@sha256:c0c132bee0f0a75e5b7cfd3d67508d977dc264a48faa7802c135f510237223d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.8 MB (442772596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2938ec3291d65143eff8ee31337a940b83a3fffaf9013183d9cb91f3b50130`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
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
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1667dd5aae8146579fcf9c985c46a2daca8bc310d3e594220b35bf045d313`  
		Last Modified: Tue, 06 Feb 2024 20:52:55 GMT  
		Size: 46.5 MB (46548250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0914260381a36f7b2d8f668f640be1af86df3eae44ba170a74dab738dd4f4a2e`  
		Last Modified: Tue, 06 Feb 2024 20:52:53 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a03eacee28055f470bcc2f23fb0491399ef8e05390067a655f47cf1df54e2b9`  
		Last Modified: Tue, 06 Feb 2024 20:53:01 GMT  
		Size: 366.9 MB (366859920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643b6211e18c63fa8f02632df7791c761ecc973de712f3a138de96dbb60a2dc8`  
		Last Modified: Tue, 06 Feb 2024 20:52:53 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8115f2c2bf01732a76a17a4d600aee7607f058a31a321ebc1869d5a3222c89`  
		Last Modified: Tue, 06 Feb 2024 20:52:54 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50b7835626fd2761d2ae767897586b62ff42680b386b05b132d0f0e80f1663b`  
		Last Modified: Tue, 06 Feb 2024 20:52:54 GMT  
		Size: 473.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0e9dc1f2098985a5653d95137b77d1bc5775f583c082dc3d7a6c219d029006`  
		Last Modified: Tue, 06 Feb 2024 20:52:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6918dd923cb291bd234ebf7c4dc807f713ba207aeaaf4773fe350d283e9026ce`  
		Last Modified: Tue, 06 Feb 2024 20:52:56 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb18af95da3e564f25a142bc91014b7dab0e900388d7db10c18ac38d2304b42b`  
		Last Modified: Tue, 06 Feb 2024 20:52:57 GMT  
		Size: 1.8 MB (1844906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de739a5cd6d25df98393b1ab0d888319eb5b10899b158565bc63d9406c242e73`  
		Last Modified: Tue, 06 Feb 2024 20:52:57 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.18` - unknown; unknown

```console
$ docker pull logstash@sha256:672dab2d811b50b308ee6b41dd0dafedc89d0642e686ea28614f17d691232d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2091562701fd1d1f67ff48e1707f8a83c77e1ebce46d721dfaafce347dd2d40`

```dockerfile
```

-	Layers:
	-	`sha256:9d14a9e8a11037e551c3431a46d5141178a32195a72c2a1535044e6f6dd179d6`  
		Last Modified: Tue, 06 Feb 2024 20:52:54 GMT  
		Size: 2.9 MB (2938728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:128c5f9f2fab22a5716435b1a723d0405edbc9c0d76c8cbd5696fa2033ebbed1`  
		Last Modified: Tue, 06 Feb 2024 20:52:53 GMT  
		Size: 32.2 KB (32168 bytes)  
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

**does not exist** (yet?)
