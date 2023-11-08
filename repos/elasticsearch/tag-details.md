<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.14`](#elasticsearch71714)
-	[`elasticsearch:8.11.0`](#elasticsearch8110)

## `elasticsearch:7.17.14`

```console
$ docker pull elasticsearch@sha256:2283a10121603e695e84313e8b794b310a1e2a9c458d3f165f20431a510423d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.17.14` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c7b7c4f45b516ff5bf6abc95488338f1e56b9d2fd14e74a79d98e32d302f6be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367415646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bea68e170705752d386e2f360713e71333b7df9383bf77facddfaafb214953`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 22:22:24 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 05 Oct 2023 22:22:25 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Oct 2023 22:22:25 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Oct 2023 22:22:25 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Oct 2023 22:22:41 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 05 Oct 2023 22:22:41 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Oct 2023 22:22:41 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 22:22:41 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Oct 2023 22:22:42 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Oct 2023 22:22:42 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Oct 2023 22:22:43 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Oct 2023 22:22:43 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Oct 2023 22:22:43 GMT
LABEL org.label-schema.build-date=2023-10-05T22:17:33.780167078Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=774e3bfa4d52e2834e4d9d8d669d77e4e5c1017f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.14 org.opencontainers.image.created=2023-10-05T22:17:33.780167078Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=774e3bfa4d52e2834e4d9d8d669d77e4e5c1017f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.14
# Thu, 05 Oct 2023 22:22:43 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Oct 2023 22:22:43 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce03a8bcc73c8878a1bd2c63a68936e8f31bc3386f0cbcfb5beac6f7ef4726b6`  
		Last Modified: Sun, 15 Oct 2023 21:41:20 GMT  
		Size: 14.1 MB (14103913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a135dee158bbec26d1f8d60aff8bd3bca9d27f83db8df03f0a0f227af41735c`  
		Last Modified: Sun, 15 Oct 2023 21:41:18 GMT  
		Size: 4.3 KB (4339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6447c6580cc6bd881aa25fec3b8f90e5948a25313d8dd2918dc882253740cba6`  
		Last Modified: Sun, 15 Oct 2023 21:41:42 GMT  
		Size: 324.4 MB (324413388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d49beb0c9d2b18f4cb3e5fc248b83a9007992c538ec5535511c2a5ba1666941`  
		Last Modified: Sun, 15 Oct 2023 21:41:21 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a9cc20930a7d1fe1e7a3baacb9e620b0188428e5aa6efe317ed4170b2f5935`  
		Last Modified: Sun, 15 Oct 2023 21:41:17 GMT  
		Size: 2.0 KB (1984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21f30d4808d368aa997e7aca2302faa3abf388e5c1d842ab20e72e278cf706f`  
		Last Modified: Sun, 15 Oct 2023 21:41:16 GMT  
		Size: 192.1 KB (192139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3bebd03fbb146490b4ab33b89e39b84152012a3ae2983a5e8622b6dd2d6d97`  
		Last Modified: Sun, 15 Oct 2023 21:41:16 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78556d8f50914c24306090f59b050ea9d57d32f6dec27189167744f649da3289`  
		Last Modified: Sun, 15 Oct 2023 21:41:15 GMT  
		Size: 109.2 KB (109243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.17.14` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d0f7cf9064bbc124a765cfc4cae4897cca33eccdd2f00d6bb4e633fa7793a414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.7 MB (362710792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc9fd861ebb65b1c3974e67ffaf503a8e0e905dad32a47b1e4616911ddf1625`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 05 Oct 2023 22:24:00 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 05 Oct 2023 22:24:02 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Oct 2023 22:24:02 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Oct 2023 22:24:02 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Oct 2023 22:24:04 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 05 Oct 2023 22:24:04 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 05 Oct 2023 22:24:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Oct 2023 22:24:05 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Oct 2023 22:24:05 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Oct 2023 22:24:05 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Oct 2023 22:24:06 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Oct 2023 22:24:06 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Oct 2023 22:24:06 GMT
LABEL org.label-schema.build-date=2023-10-05T22:17:33.780167078Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=774e3bfa4d52e2834e4d9d8d669d77e4e5c1017f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.14 org.opencontainers.image.created=2023-10-05T22:17:33.780167078Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=774e3bfa4d52e2834e4d9d8d669d77e4e5c1017f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.14
# Thu, 05 Oct 2023 22:24:06 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Oct 2023 22:24:06 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1527c3d34f6dbcd2d497bb04cd79773b5470c9ee598bbe1f592495ff0c1f7d`  
		Last Modified: Thu, 02 Nov 2023 23:40:35 GMT  
		Size: 12.9 MB (12853835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6208089f8a98805e375a073eb608564601514f0219e8f69db14ca33f7e7d86a7`  
		Last Modified: Thu, 02 Nov 2023 23:40:33 GMT  
		Size: 4.4 KB (4357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf64e867920b9c94613a084b44db7fbe97e79859bc076992d9e8e2bd509a32c6`  
		Last Modified: Thu, 02 Nov 2023 23:40:52 GMT  
		Size: 322.3 MB (322345079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87076fbd4cb01c68c48b2fa981718ed64e1cc9e38e97102806fe7b728801642f`  
		Last Modified: Thu, 02 Nov 2023 23:40:31 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c1393344f7f80e266e3e2e30a3682db05271224129b05afaebe4e1085c4474`  
		Last Modified: Thu, 02 Nov 2023 23:40:31 GMT  
		Size: 2.0 KB (1983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395bc23cbc3d289367e4e75dfed87d93be0b7b21120edd3d00bcc7747c6a6e6c`  
		Last Modified: Thu, 02 Nov 2023 23:40:31 GMT  
		Size: 186.2 KB (186163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7705b912b1248807b93bb078c794e0d254f908d516f1d0b6e7a11e17723391d2`  
		Last Modified: Thu, 02 Nov 2023 23:40:31 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb67150a47fb253abf189c118218a617eca7e5c20afe6670b391c71417815e7`  
		Last Modified: Thu, 02 Nov 2023 23:40:31 GMT  
		Size: 109.2 KB (109248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.11.0`

```console
$ docker pull elasticsearch@sha256:d912ab6a75aa8a89307eb21ad6af61c3a34bbc0a74c5c697f42dd3a633962e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.11.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2ed1d6881b5b846cb02559ba35ea4351b45ac8809bfb00681151a92cedf24cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.4 MB (674351579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f03b6ec0c6f6d9a844550d1b3689e868e11850ac4e668e8583490c96baca8f1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Sat, 04 Nov 2023 10:11:35 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Sat, 04 Nov 2023 10:11:36 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Sat, 04 Nov 2023 10:11:36 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 04 Nov 2023 10:11:36 GMT
WORKDIR /usr/share/elasticsearch
# Sat, 04 Nov 2023 10:11:58 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Sat, 04 Nov 2023 10:11:58 GMT
COPY /bin/tini /bin/tini # buildkit
# Sat, 04 Nov 2023 10:11:58 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2023 10:11:58 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Sat, 04 Nov 2023 10:12:05 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Sat, 04 Nov 2023 10:12:05 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Sat, 04 Nov 2023 10:12:07 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Sat, 04 Nov 2023 10:12:07 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Sat, 04 Nov 2023 10:12:07 GMT
LABEL org.label-schema.build-date=2023-11-04T10:04:57.184859352Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d9ec3fa628c7b0ba3d25692e277ba26814820b20 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.0 org.opencontainers.image.created=2023-11-04T10:04:57.184859352Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d9ec3fa628c7b0ba3d25692e277ba26814820b20 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.0
# Sat, 04 Nov 2023 10:12:07 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Sat, 04 Nov 2023 10:12:07 GMT
CMD ["eswrapper"]
# Sat, 04 Nov 2023 10:12:07 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe7f22b2664253efb82b68d9a5781ed83c03fd61c12156df34f00f0a68c0e53`  
		Last Modified: Wed, 08 Nov 2023 00:26:40 GMT  
		Size: 7.5 MB (7509916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bc203aaf8b598448743cc070129f1a57e67ded1d269f59cc0b917fc33a8a2d`  
		Last Modified: Wed, 08 Nov 2023 00:26:38 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201b50702da3a4d894fe97d2d4acc5d4e50891365cca4deb47566de8d6c644a1`  
		Last Modified: Wed, 08 Nov 2023 00:27:33 GMT  
		Size: 637.9 MB (637943823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fc15ec9a941bd88aac3895939ce02f09dd3246e8f51bbc427583a82e97d5aa`  
		Last Modified: Wed, 08 Nov 2023 00:26:36 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7327152092a616af0aca7d711c64858ffabbb45102bcab9a3c44dbd3811ac108`  
		Last Modified: Wed, 08 Nov 2023 00:26:36 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f9461950aa5be820c270641e95ffee9644e3f1bc475dddc83911c2fdeb539`  
		Last Modified: Wed, 08 Nov 2023 00:26:36 GMT  
		Size: 191.9 KB (191882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb7a77c34b7b62671509bb7f4bef66ca4697da2624c9b87aedc286fa673c215`  
		Last Modified: Wed, 08 Nov 2023 00:26:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd0802b3468fd91dc2fb4fc4eb2f41440065e82f394742d9a95e60cfb253f78`  
		Last Modified: Wed, 08 Nov 2023 00:26:39 GMT  
		Size: 109.2 KB (109239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.11.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b59dfd735d101120bb6cb57230a04ce7c06fb328e7a743f9c93a64f418b3b264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.0 MB (451992726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6435e9be51cc0e5ba8b6746892bae1cacf974262a08857b1c8d4a0241b85fee1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Sat, 04 Nov 2023 10:12:39 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Sat, 04 Nov 2023 10:12:43 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Sat, 04 Nov 2023 10:12:43 GMT
ENV ELASTIC_CONTAINER=true
# Sat, 04 Nov 2023 10:12:43 GMT
WORKDIR /usr/share/elasticsearch
# Sat, 04 Nov 2023 10:12:48 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Sat, 04 Nov 2023 10:12:48 GMT
COPY /bin/tini /bin/tini # buildkit
# Sat, 04 Nov 2023 10:12:48 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2023 10:12:48 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Sat, 04 Nov 2023 10:12:52 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Sat, 04 Nov 2023 10:12:52 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Sat, 04 Nov 2023 10:12:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Sat, 04 Nov 2023 10:12:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Sat, 04 Nov 2023 10:12:54 GMT
LABEL org.label-schema.build-date=2023-11-04T10:04:57.184859352Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d9ec3fa628c7b0ba3d25692e277ba26814820b20 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.11.0 org.opencontainers.image.created=2023-11-04T10:04:57.184859352Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d9ec3fa628c7b0ba3d25692e277ba26814820b20 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.0
# Sat, 04 Nov 2023 10:12:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Sat, 04 Nov 2023 10:12:54 GMT
CMD ["eswrapper"]
# Sat, 04 Nov 2023 10:12:54 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b7fce9281e3afe428ea22b2d0da41999a20290ba20993fdf2d336733b323bf`  
		Last Modified: Tue, 07 Nov 2023 23:42:43 GMT  
		Size: 7.3 MB (7330723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1098896b92da1cfd88f11c251a1f0f10d59be1cc8ccde2dde821411eee84944e`  
		Last Modified: Tue, 07 Nov 2023 23:42:42 GMT  
		Size: 4.4 KB (4356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4112cc587f28c9849a6b4d06446fbc0bead1e0b0a12f5d4a2cc0da61af1bf09e`  
		Last Modified: Tue, 07 Nov 2023 23:43:03 GMT  
		Size: 417.2 MB (417151732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ccd21d2d57c1dc3964f65983aa45b2a8e27e89e5d9e811e0ff28e5c802ce1c`  
		Last Modified: Tue, 07 Nov 2023 23:42:39 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f00d26bc538e2b7ac5aec6408335fe3e07701d3ecf79e005d1b07b571c6080`  
		Last Modified: Tue, 07 Nov 2023 23:42:39 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a81a8d5c2aad8e7b8b1cd30146764bd94c3844aec6158edc4370771dc95220`  
		Last Modified: Tue, 07 Nov 2023 23:42:39 GMT  
		Size: 185.9 KB (185902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c1431ac2e95f1addcb9cc00cdcae71cc3976acaa41aaf4e6a1dc37ddf86bf0`  
		Last Modified: Tue, 07 Nov 2023 23:42:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7241b5cb1d4aad2ef0ecc1678f40ac77a8876c63b28c6f6f1d5a5dca6e8e3526`  
		Last Modified: Tue, 07 Nov 2023 23:42:43 GMT  
		Size: 109.2 KB (109244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
