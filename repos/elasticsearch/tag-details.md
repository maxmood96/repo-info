<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.23`](#elasticsearch71723)
-	[`elasticsearch:8.14.3`](#elasticsearch8143)

## `elasticsearch:7.17.23`

```console
$ docker pull elasticsearch@sha256:fa9f4b9dc351278ea3ca6f230b4baffaac35d5bcd985437b7a254708b6ccf78b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.23` - linux; amd64

```console
$ docker pull elasticsearch@sha256:855170c54428079915866edb0b08a67329a1bdbe60fb52cd108d16aa46a68602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362606418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8dcae8769c3d51e1eb24ca90844dd084cae50c32f4964a6ebf9d5d51fa63138`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.build-date=2024-07-25T14:37:42.448799567Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=61d76462eecaf09ada684d1b5d319b5ff6865a83 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.23 org.opencontainers.image.created=2024-07-25T14:37:42.448799567Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=61d76462eecaf09ada684d1b5d319b5ff6865a83 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.23
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5405c7b1cbe4273415abacce507d08c06de67f80b1e4887f13b62c143f7ff0aa`  
		Last Modified: Tue, 30 Jul 2024 23:56:04 GMT  
		Size: 7.5 MB (7513044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e8145a6950535e635a34e073ef37e14a03ea0ace339b528d36a2edebfcd440`  
		Last Modified: Tue, 30 Jul 2024 23:56:04 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127c6ecc5d1949a63e92eb71e629bb0f5200d39079878276fc7519b817e9428`  
		Last Modified: Tue, 30 Jul 2024 23:56:09 GMT  
		Size: 327.3 MB (327263921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4bed4283f91e4eec8a6c1a3186cf012dd5190d6588b49a12eb030e898c5649`  
		Last Modified: Tue, 30 Jul 2024 23:56:04 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80d576913a915a850d7c9837cf8186318d8a66add6eecaba3a6d158ff520f2a`  
		Last Modified: Tue, 30 Jul 2024 23:56:05 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30674c8fd4512ec986fdf661ea97500171abdf0faf0299efa2be00c1065d712`  
		Last Modified: Tue, 30 Jul 2024 23:56:05 GMT  
		Size: 192.2 KB (192172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e544319d2658d134440aff7507a4a382adf419ac91bb12a99b869ec110fcf01`  
		Last Modified: Tue, 30 Jul 2024 23:56:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4542148b7852aa354f4296ad237c2003e1be523585ecf5e2adedc7542243cb53`  
		Last Modified: Tue, 30 Jul 2024 23:56:06 GMT  
		Size: 109.3 KB (109254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.23` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0e82319899785991a24dc8653976169d9511f93e98a724bdd9d4c0a2cc672517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03448664f8b1c0b17cf5b54cedcfaf33b5c8c9bcdccc3fa9d64ecce16175018`

```dockerfile
```

-	Layers:
	-	`sha256:9eb3083bbd73550e3054c653311850b0ad45f6288371f71e3270b99a3517f5bb`  
		Last Modified: Tue, 30 Jul 2024 23:56:04 GMT  
		Size: 2.4 MB (2367247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4221b845f5bc478c64e0e7331f35e4a324e542e58ca80a5986d9d4f3a3aa8979`  
		Last Modified: Tue, 30 Jul 2024 23:56:04 GMT  
		Size: 37.6 KB (37634 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.23` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:4528e343dc6107141c85903b8f4bc44d88c8cb893e459766870794e14ec9ac7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358539453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6def07c3688cc742c49c1fa0a53d13f4886448b504c8e673d0b09815660553`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.build-date=2024-07-25T14:37:42.448799567Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=61d76462eecaf09ada684d1b5d319b5ff6865a83 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.23 org.opencontainers.image.created=2024-07-25T14:37:42.448799567Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=61d76462eecaf09ada684d1b5d319b5ff6865a83 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.23
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8182df016d3810f1028ce9f9735909dd0694ecbac2832068e2c7de5e294c66`  
		Last Modified: Tue, 30 Jul 2024 23:57:51 GMT  
		Size: 7.3 MB (7332143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ddafb9279fa526c88ef4fdf9ee022ca57dd0ea9b71785e4585d2bc40aefad8`  
		Last Modified: Tue, 30 Jul 2024 23:57:51 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3535a43f6f6c0325bfd4f3050f166b56a118a613c399128b302a5eec672999c3`  
		Last Modified: Tue, 30 Jul 2024 23:57:58 GMT  
		Size: 324.9 MB (324921830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3611e673b53e3638ddc799cc45d3271fe76e97b415395c60850d32a49f7c68`  
		Last Modified: Tue, 30 Jul 2024 23:57:51 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ac925e2156cf8e972f293fa223d055106f1d407d3079c8a7e4f07dff710bdf`  
		Last Modified: Tue, 30 Jul 2024 23:57:52 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d025977291e93e85d4d19c42620bd5767a0c2fb832fe412e96673142a6de48c`  
		Last Modified: Tue, 30 Jul 2024 23:57:52 GMT  
		Size: 186.2 KB (186179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f4f947ac9258e924a04cb2ef3428d170b8716927924e21c06c20f58cdf0270`  
		Last Modified: Tue, 30 Jul 2024 23:57:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf30e88740c5551075f8c8b34986db4ee80583c3cd7fbdc7202610ef1ab1821`  
		Last Modified: Tue, 30 Jul 2024 23:57:53 GMT  
		Size: 109.3 KB (109251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.23` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b6083225f44e323bd7e316605a3e6e3e475a4010cf82535d20effcac579e21d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5519682904a76962fbbf9519fdd903f42736dbc19d1f8e3ebe2b3bcbadb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:998dde55e2b08b10783833caae8266b48da3e6de4be664734aca2593f95605c5`  
		Last Modified: Tue, 30 Jul 2024 23:57:51 GMT  
		Size: 2.4 MB (2367479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd9411a1c262d7d399f6b162b2e8323fd7ec733e5b12215055679f87a5f958a`  
		Last Modified: Tue, 30 Jul 2024 23:57:51 GMT  
		Size: 37.9 KB (37899 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.14.3`

```console
$ docker pull elasticsearch@sha256:1ddbb1ae0754278f3ab53edc24fcc5c790ebc2422cc47abea760b24abee2d88a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.14.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a2dd3751a14b3065599b6c9a03b98e3ccdea38b4cce3e6175e06b2e687c09b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.7 MB (629677670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482b5962b08aec7c83a8af3c8aa2213d9a55ff6d6fea7ae2c2fcd9721dbf7299`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 08:06:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jul 2024 08:06:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 11 Jul 2024 08:06:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 11 Jul 2024 08:06:13 GMT
LABEL org.label-schema.build-date=2024-07-07T22:04:49.882652950Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d55f984299e0e88dee72ebd8255f7ff130859ad0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.14.3 org.opencontainers.image.created=2024-07-07T22:04:49.882652950Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d55f984299e0e88dee72ebd8255f7ff130859ad0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.3
# Thu, 11 Jul 2024 08:06:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Jul 2024 08:06:13 GMT
CMD ["eswrapper"]
# Thu, 11 Jul 2024 08:06:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f01394c961642feba99833afd6e5b72eece97f65788aa93e14b758678b5156`  
		Last Modified: Thu, 11 Jul 2024 18:00:09 GMT  
		Size: 7.5 MB (7513089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14877811f740b24a4ce715b7e9f6e52121aefe6669ba1da1420292c13f47347`  
		Last Modified: Thu, 11 Jul 2024 18:00:09 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947b5a7f8b6172d2c03c73c9a4c46718125d632a8e45327eec9b945d152b495f`  
		Last Modified: Thu, 11 Jul 2024 18:00:19 GMT  
		Size: 594.3 MB (594335675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d31234dbb5c647aec75e8a5701a7c6bedc26002fbfc9577ba11e4993a7196f5`  
		Last Modified: Thu, 11 Jul 2024 18:00:10 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70362de5376682e204928a75204d38e725fbbdc7593ea9ac6bb00d37985d1573`  
		Last Modified: Thu, 11 Jul 2024 18:00:10 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe6af6dc09451dabafaa0926aa68948a1298355069d3497fbadb49b7fc73f4e`  
		Last Modified: Thu, 11 Jul 2024 18:00:10 GMT  
		Size: 191.9 KB (191897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f706f54d11b27ba064bbfe047fb467de2f4c81f283b2bb293743fea4014f20`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fefb920fd9f78d5ffe5c3c3ea77265236113e02e4f3fe2145fce54f8ad1040`  
		Last Modified: Thu, 11 Jul 2024 18:00:11 GMT  
		Size: 109.2 KB (109246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.14.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c045006a04b803f37200f40377ade88060a9ae07aaa71512a0aa3e2f8f53fc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6b2a3a9c761aff1bfc5a31d09f779605681b826bd37147bfce4533a13e593d`

```dockerfile
```

-	Layers:
	-	`sha256:077a6cb3069fc09a9d65910d2ff385bbc63018f3500c5e11e420caacdceb5435`  
		Last Modified: Thu, 11 Jul 2024 18:00:09 GMT  
		Size: 2.6 MB (2594341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8943902b07f158122ad468d85ae3ea806a5aae8ffab710eaae43f58a63457251`  
		Last Modified: Thu, 11 Jul 2024 18:00:09 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.14.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c36e6d78c75781986589729963e3a7bfb08ddea67d862f6bd2cfe319ce5ab1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.8 MB (473779581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c359bb77b58216a54a4d53a7fa95f9ded45f3b19a647e85be1f7e87bca48953d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 11 Jul 2024 08:06:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 11 Jul 2024 08:06:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 11 Jul 2024 08:06:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 11 Jul 2024 08:06:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 11 Jul 2024 08:06:13 GMT
LABEL org.label-schema.build-date=2024-07-07T22:04:49.882652950Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d55f984299e0e88dee72ebd8255f7ff130859ad0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.14.3 org.opencontainers.image.created=2024-07-07T22:04:49.882652950Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d55f984299e0e88dee72ebd8255f7ff130859ad0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.14.3
# Thu, 11 Jul 2024 08:06:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Jul 2024 08:06:13 GMT
CMD ["eswrapper"]
# Thu, 11 Jul 2024 08:06:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918ce06f3ebdd8fad176f7e7b06b32bb2e58ec533924c4527290efd4a012f77d`  
		Last Modified: Mon, 08 Jul 2024 18:05:17 GMT  
		Size: 7.3 MB (7332124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c67457edb7cfc5cffdf9c4e2a2536ef5c4fe78798f863acba17125b6abc9cb`  
		Last Modified: Mon, 08 Jul 2024 18:05:16 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f8b5c24e985cacf1919d6c8b5481fe963700b5581ad5ae65c38f043a08145`  
		Last Modified: Thu, 11 Jul 2024 18:00:45 GMT  
		Size: 440.2 MB (440162470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d597e584ad2f31416c78f48ed5d578dad22000115d736687303116b4583a5c5`  
		Last Modified: Thu, 11 Jul 2024 18:00:36 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8544774e1fac869670e803191ff2377e7c980698c7ca93da45721295505bbaa`  
		Last Modified: Thu, 11 Jul 2024 18:00:36 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e862c67af347a812c03add9c36551a02c05e5beced08318607f5b1c4a591a2fb`  
		Last Modified: Thu, 11 Jul 2024 18:00:36 GMT  
		Size: 185.9 KB (185925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1c2618377d8ad25fb22e9ca63d26389631b6e2a8ca4b1673b93a2cba1a05c`  
		Last Modified: Thu, 11 Jul 2024 18:00:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9837b875bdb12ffc59e0fbe2171f864cc7bd57f33f0a77874eb7f125f8b29fc`  
		Last Modified: Thu, 11 Jul 2024 18:00:37 GMT  
		Size: 109.3 KB (109257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.14.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1c38a9fc78bafda1590eebddb512f8ef796066f8257f5040a7da3f15c586ba91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1b1b96511eadc0acbb1281e0e40a27a6f85edb57e880f645467d53c2e7093e`

```dockerfile
```

-	Layers:
	-	`sha256:43d531fb533c2d291cf1a6620b0aee99df32f97529bcc04f8b13210db42f540a`  
		Last Modified: Thu, 11 Jul 2024 18:00:37 GMT  
		Size: 2.6 MB (2594581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b23f52db7b28fa8c0f4fcb0827d414082f73a1fc8b25566329b96e3abe070d2`  
		Last Modified: Thu, 11 Jul 2024 18:00:36 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json
