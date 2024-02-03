<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.17`](#elasticsearch71717)
-	[`elasticsearch:8.12.0`](#elasticsearch8120)

## `elasticsearch:7.17.17`

```console
$ docker pull elasticsearch@sha256:f867a97999c818f4370b8b2206b31015b532edb90db58e26015f7c3c9427a7ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.17` - linux; amd64

```console
$ docker pull elasticsearch@sha256:af59db0adbd6b14ca4d2d1ab902b50119774896511d3650fd08be97edad1ebbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.2 MB (364218127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6541ba64881338575e43803fa009fab709939d2b824817b459bc84a0c9c57e1e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 23 Jan 2024 14:25:39 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jan 2024 14:25:39 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 23 Jan 2024 14:25:39 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 14:25:39 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 23 Jan 2024 14:25:39 GMT
LABEL org.label-schema.build-date=2024-01-18T10:05:03.821431920Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aba4da413a368e296dfc64fb20897334d0340aa1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.17 org.opencontainers.image.created=2024-01-18T10:05:03.821431920Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=aba4da413a368e296dfc64fb20897334d0340aa1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.17
# Tue, 23 Jan 2024 14:25:39 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 23 Jan 2024 14:25:39 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70904ec905d15ddc28a87d7a0651cf93e5c2158d303801407053e3e4d9b23253`  
		Last Modified: Fri, 02 Feb 2024 00:56:04 GMT  
		Size: 7.5 MB (7509256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531abde8d8ed5eb67d6ee5e717821f02d45f5880d1662fd8df1282df22d5c2f5`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834d0fc2ad24c67d29a42d624b924b08db4d7bb197d07f5147759aea330aa66`  
		Last Modified: Fri, 02 Feb 2024 00:56:07 GMT  
		Size: 328.9 MB (328876289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99cc4bcce2fd3046f7857fc49cf40036dfa7facf1dcd1fb0f8996ea28639eff`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0219004b84d5e0bf1b60977bb7db3bb2171d5b48ec3fb86c82983ec185d75`  
		Last Modified: Fri, 02 Feb 2024 00:56:02 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e1e011f7907426be7aa988b6b929666e04145c84fbc69638341f7267d4f8f6`  
		Last Modified: Fri, 02 Feb 2024 00:56:02 GMT  
		Size: 192.1 KB (192146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48161179b2bcf2899d39a63c0589c04c4d552486b3e1c377a83d4a7fad3f4d03`  
		Last Modified: Fri, 02 Feb 2024 00:56:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcf7a95f6ec130e5d0f8a1223bcf14de6ff91640e8f3c92f12d217c11d77ac7`  
		Last Modified: Fri, 02 Feb 2024 00:56:04 GMT  
		Size: 109.2 KB (109250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.17` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:361db746988022067f2cf22bf6af194c5695acabb21b74cf96ab3a3966539611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2107280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f990cf606c03902276527159d33c1287b06e7f5ab3333b5f1337a62443ed71`

```dockerfile
```

-	Layers:
	-	`sha256:4850fd00034dd19d8bdbba9fbbee13f99db03c962e7fe0577a74db25ea533039`  
		Last Modified: Fri, 02 Feb 2024 00:56:02 GMT  
		Size: 2.1 MB (2069539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a74eae8e053d480822bd5671a985678258bc2a10ee681afaf7be8da0b6db9d`  
		Last Modified: Fri, 02 Feb 2024 00:56:02 GMT  
		Size: 37.7 KB (37741 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.17` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:97cec74ea110d3b71bb305365acf8434298365fb8a2049a50ce21fc8291244ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360387319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44603637c39f9014feea309a83c26782399906cb64828c3baa8930d2965fa299`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 23 Jan 2024 14:25:39 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jan 2024 14:25:39 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 23 Jan 2024 14:25:39 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 14:25:39 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 23 Jan 2024 14:25:39 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 23 Jan 2024 14:25:39 GMT
LABEL org.label-schema.build-date=2024-01-18T10:05:03.821431920Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aba4da413a368e296dfc64fb20897334d0340aa1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.17 org.opencontainers.image.created=2024-01-18T10:05:03.821431920Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=aba4da413a368e296dfc64fb20897334d0340aa1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.17
# Tue, 23 Jan 2024 14:25:39 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 23 Jan 2024 14:25:39 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111d4c2b87a53ae05073db1e549a497aaadab7083e7376fb16c0884a05e4f9d8`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 7.3 MB (7328596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2159b8ae36baed42e8be2dfb6aff2e12ffadada674ae811498b9c4ff306f98a7`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abbeebb7a4a2e1bbccd2544206ec5450f3eb0ad33deb2adbed919ab1f72ebec`  
		Last Modified: Fri, 02 Feb 2024 22:11:34 GMT  
		Size: 326.8 MB (326771897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2d34bd55d18465b50ccca8ecddfa01337b5854b800b1234d70fe19c163750f`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d38ac33343e13efd4de411519f1dc0b50e576ddb8959acac0cdacdeaf2e52db`  
		Last Modified: Fri, 02 Feb 2024 22:11:27 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eec67111bc7cd209d5a3f1b6f1554662573cf8f98b4607dfe7b576ae003c23`  
		Last Modified: Fri, 02 Feb 2024 22:11:27 GMT  
		Size: 186.1 KB (186147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962a8ae26248be8a7a0802dac2db98e3318a4ce92ab39e9683ecc1fc38a520e7`  
		Last Modified: Fri, 02 Feb 2024 22:11:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddb36b81afe5c0c86fa9310966e878ce8097fa426b4cf189301265075633540`  
		Last Modified: Fri, 02 Feb 2024 22:11:28 GMT  
		Size: 109.2 KB (109249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.17` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:38d57a97e28cc0822d5cd00dd3b69dd97e3209474968d20bdc807e8887405445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2111693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb00d406cd2d52372b115f5d8b7676fc3f746014667f1e5475a0b60b979524a0`

```dockerfile
```

-	Layers:
	-	`sha256:89eef951e42b9be4da5a0a89a789e5ecb15118e0d35d218e7970c2fe9cf06b8a`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 2.1 MB (2073947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7737fce6a27b0bba8b53f164abacb94823a9d8d48b51d6ae70f6b778f12e095`  
		Last Modified: Fri, 02 Feb 2024 22:11:26 GMT  
		Size: 37.7 KB (37746 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.12.0`

```console
$ docker pull elasticsearch@sha256:2529e4b8062e4b9f0a31bea3ee797a58dae4cfe2d2b5879b4a1b03250c7ad31c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.12.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5c2833bb301606230e4e7d89a263ca089c1a68e150ccdde952b057d0f18845cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.6 MB (663583093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e28e876ca5b81892efb4dc60771935f028a3fe48e1b332bca8013b21c3e081`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 17 Jan 2024 15:49:20 GMT
ARG RELEASE
# Wed, 17 Jan 2024 15:49:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Jan 2024 15:49:20 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.build-date=2024-01-11T10:05:27.953830042Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1665f706fd9354802c02146c1e6b5c0fbcddfbc9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.0 org.opencontainers.image.created=2024-01-11T10:05:27.953830042Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1665f706fd9354802c02146c1e6b5c0fbcddfbc9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.0
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["eswrapper"]
# Wed, 17 Jan 2024 15:49:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5174fdea5e2c4a00d6c3f9167ab5d2134bd04e143be2dc8d1af600f9e924d9`  
		Last Modified: Fri, 02 Feb 2024 00:56:45 GMT  
		Size: 7.5 MB (7509258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44589f5973c38a465755a94073568680e4e995714dfb4edf847dbb0aa3a6369c`  
		Last Modified: Fri, 02 Feb 2024 00:56:45 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5380ac5f0ffa058b443e17dfb9c867a5e729e2366105eab1dbcf204b194dcfcc`  
		Last Modified: Fri, 02 Feb 2024 00:57:23 GMT  
		Size: 628.2 MB (628241777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9aabfce0822d0fb98f63850c320c05510c3bd5fb8ac0bb6907a7f2bcf365`  
		Last Modified: Fri, 02 Feb 2024 00:56:45 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e7b5ed696279774038960e48e959feac9812563af492ee8d58c9c214b9a726`  
		Last Modified: Fri, 02 Feb 2024 00:56:46 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281ed3b728c7a87f72d1c200e49f64ead2ac30af53ce3a2c5847e212a9883ff7`  
		Last Modified: Fri, 02 Feb 2024 00:56:46 GMT  
		Size: 191.9 KB (191878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c53121228d64a60ff4d391e01b82a6cafc4c2d51f81f55d87f3c78cbbea10cb`  
		Last Modified: Fri, 02 Feb 2024 00:56:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f7827663db372a853c85cffceeb8b2eb94da46648bc25e1a0971ca9fe55613`  
		Last Modified: Fri, 02 Feb 2024 00:56:47 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:af4b8ff33725ff17ede500e92932d3e2319247abf1af5a465d90f44c47d97a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c832c5b84dc12fcaeb6fef802be169415cd46560ae75874c23af7c016c9d22`

```dockerfile
```

-	Layers:
	-	`sha256:53c12028f72267bc36c3e3034717e1c9f98b6eaa32516d701e128a7dbbb14082`  
		Last Modified: Fri, 02 Feb 2024 00:56:45 GMT  
		Size: 2.3 MB (2342801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a23907739eb5c74a575905467169f4696cc693076e90e4c965816bd49ec2e6a`  
		Last Modified: Fri, 02 Feb 2024 00:56:45 GMT  
		Size: 37.8 KB (37758 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.12.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:70844485d4403a346c70942535eeed46ff61df0f54beeb355a6b8f57fbfa13b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.6 MB (456554852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b23bf20e903727685868dd6c1533d98f21bb038930907796af5c721ea406323`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 17 Jan 2024 15:49:20 GMT
ARG RELEASE
# Wed, 17 Jan 2024 15:49:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 17 Jan 2024 15:49:20 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 15:49:20 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 17 Jan 2024 15:49:20 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 17 Jan 2024 15:49:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 17 Jan 2024 15:49:20 GMT
LABEL org.label-schema.build-date=2024-01-11T10:05:27.953830042Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1665f706fd9354802c02146c1e6b5c0fbcddfbc9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.12.0 org.opencontainers.image.created=2024-01-11T10:05:27.953830042Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1665f706fd9354802c02146c1e6b5c0fbcddfbc9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.0
# Wed, 17 Jan 2024 15:49:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 15:49:20 GMT
CMD ["eswrapper"]
# Wed, 17 Jan 2024 15:49:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7036eeda0b893893c3d530238575da4fe4c4ae51c9fd09e8694567e7d8780e7`  
		Last Modified: Fri, 02 Feb 2024 22:10:05 GMT  
		Size: 7.3 MB (7328581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c108c9129f02502270742d354eb48ccdca567cdcf1a506749a03c9b3bf38d`  
		Last Modified: Fri, 02 Feb 2024 22:10:05 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eedbcc153b0d8c3c81e0150e6c9faba89a55a31454cbbbbd0c44b356db2bf9`  
		Last Modified: Fri, 02 Feb 2024 22:10:15 GMT  
		Size: 422.9 MB (422939934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3483fd007414258f79e008c965f34816cd6834dd6c1ed393efb856dc33d283ae`  
		Last Modified: Fri, 02 Feb 2024 22:10:06 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc35d548cabf6bb27ed99e3a4b84295e40a234fdf2ed96c5119c4cb0abe50d0`  
		Last Modified: Fri, 02 Feb 2024 22:10:07 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b97919acd6f04a5b6b4a98de213a615c85ee8bd25aafd118ccaa3743194695`  
		Last Modified: Fri, 02 Feb 2024 22:10:07 GMT  
		Size: 185.9 KB (185906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319dce762c96cf542539582ece7ac45d2bf4a5403159e16aa69f297c139df7f`  
		Last Modified: Fri, 02 Feb 2024 22:10:07 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13ad8b7ec46d4b98ef8e5f0120e641c7554dea1c9f8e9efb37a7fa8b0f678ae`  
		Last Modified: Fri, 02 Feb 2024 22:10:08 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c4b547509edcc9511ddf99f3b52b231a49d527ea3c9ffa35ff39989965279fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93557f4f40c4a142175c111ff7ddc16011d31b31a89c90226bf0c72ee21cfd6c`

```dockerfile
```

-	Layers:
	-	`sha256:f52be9f4ce91ddf68b67e53893effb918bc56c8066e68234d69b31f892a0feea`  
		Last Modified: Fri, 02 Feb 2024 22:10:05 GMT  
		Size: 2.4 MB (2351431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb8aef1a1c135a3a702ac74776494f572f5f1eb8312390c46e2d97afc6f3c58`  
		Last Modified: Fri, 02 Feb 2024 22:10:05 GMT  
		Size: 37.8 KB (37761 bytes)  
		MIME: application/vnd.in-toto+json
