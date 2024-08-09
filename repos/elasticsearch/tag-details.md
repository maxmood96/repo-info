<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.23`](#elasticsearch71723)
-	[`elasticsearch:8.15.0`](#elasticsearch8150)

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

## `elasticsearch:8.15.0`

```console
$ docker pull elasticsearch@sha256:6f6e73f1b9d7e1b60780818f19d8d386a5fe2b6c4c397b917762284e8fba7026
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e256e117467fcd2317f4ccffb4c7517a592b4493339ea2291be47b81fbae6c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647099888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c42a6c7cdf23de38d08ae785a45a23582684530374cdb5fb94dcc40576124e`
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
# Thu, 08 Aug 2024 13:05:51 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 08 Aug 2024 13:05:51 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 08 Aug 2024 13:05:51 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.label-schema.build-date=2024-08-05T10:05:34.233336849Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1a77947f34deddb41af25e6f0ddb8e830159c179 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.0 org.opencontainers.image.created=2024-08-05T10:05:34.233336849Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1a77947f34deddb41af25e6f0ddb8e830159c179 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.0
# Thu, 08 Aug 2024 13:05:51 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 08 Aug 2024 13:05:51 GMT
CMD ["eswrapper"]
# Thu, 08 Aug 2024 13:05:51 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a482ac3512187efc27e2deb18c435aff64eb608c509f26dd75a7cf95b811fc`  
		Last Modified: Thu, 08 Aug 2024 22:57:26 GMT  
		Size: 7.5 MB (7513907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6017a3f450c5a588f36d92ad511b209e531f6d9004a8eef502e5fa43a05c491`  
		Last Modified: Thu, 08 Aug 2024 22:57:26 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4486b84b59a0174dc0b1a7db5bc0dc1787995b4e506b25fadf3e4dfc03a1eb4f`  
		Last Modified: Thu, 08 Aug 2024 22:57:35 GMT  
		Size: 611.8 MB (611757051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aabe14408da373a603f6f541a61112bc9a7f6811a0becbb8536b650f32f756`  
		Last Modified: Thu, 08 Aug 2024 22:57:26 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cef4dd10e6ec5037cbdb22dbceb890ea59ddbae1dcaa4fcb33a1a936c50f12`  
		Last Modified: Thu, 08 Aug 2024 22:57:27 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0021794561287fe10baa597958fccf30423648cc686a0a78fe409b5f56cdb61b`  
		Last Modified: Thu, 08 Aug 2024 22:57:27 GMT  
		Size: 191.9 KB (191907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1463ca4646b9960b9c07bc965d7590c8c5623061690961e0383d5f47330bd5ad`  
		Last Modified: Thu, 08 Aug 2024 22:57:27 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa3c9b658705e3e4e7ff249998b2f50f736cfd3d309a2c7b5e4b892bc29df68`  
		Last Modified: Thu, 08 Aug 2024 22:57:27 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9908ed741aeac956f0797ac75df9d3697a68f8b06e391434f8c1338cbd5af9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5310df43018059d39426b70bb5b88c055df439fd48521310f2d07dfd434ff1`

```dockerfile
```

-	Layers:
	-	`sha256:30d316df69c6b66d5336e6c3329b43196fa6bfa2ddb0239a3e3a8dac12be9bb7`  
		Last Modified: Thu, 08 Aug 2024 22:57:26 GMT  
		Size: 2.7 MB (2715496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7c9af3b25beee0590cb94190f9c41d2177d9f2a6e7628edeb589acd193f1ff`  
		Last Modified: Thu, 08 Aug 2024 22:57:26 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:5638c32105d64a51aa963c616cf730a8996938b70dbe787238b1b0d9f519b5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491202081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23cbcfda06397c9dc3e1de1de1a58429f2b966635dd611bb5d16950299091cd`
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
# Thu, 08 Aug 2024 13:05:51 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 08 Aug 2024 13:05:51 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 08 Aug 2024 13:05:51 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.label-schema.build-date=2024-08-05T10:05:34.233336849Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1a77947f34deddb41af25e6f0ddb8e830159c179 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.0 org.opencontainers.image.created=2024-08-05T10:05:34.233336849Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1a77947f34deddb41af25e6f0ddb8e830159c179 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.0
# Thu, 08 Aug 2024 13:05:51 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 08 Aug 2024 13:05:51 GMT
CMD ["eswrapper"]
# Thu, 08 Aug 2024 13:05:51 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33002d44f02da5e23ed6603f5d48bd4af7ac1dac2cfb660c6924aa5c7eb2050`  
		Last Modified: Thu, 08 Aug 2024 22:58:29 GMT  
		Size: 7.3 MB (7333110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022b9b65cceddaf23360d7395ee8e2af56ff0dcf67072b1ced575e942c9b0d9`  
		Last Modified: Thu, 08 Aug 2024 22:58:28 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5328ce029fa8d27475de2c21e1683a609ef17a22b78fc38b91951590bab38c07`  
		Last Modified: Thu, 08 Aug 2024 22:58:37 GMT  
		Size: 457.6 MB (457584015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbb19e3f51ab67cb7a41fb1ad267c6a55772f2b4a0fda0771a9a252cf20350c`  
		Last Modified: Thu, 08 Aug 2024 22:58:28 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da144797f0020fd1e5ef03f8e9fc1fa814f33a5c88b9a989d2047a881bc6540`  
		Last Modified: Thu, 08 Aug 2024 22:58:29 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c71de1a3a87d02ad4a6013e5f63475ab48decdf9b02db8bcab1800db0aa33e`  
		Last Modified: Thu, 08 Aug 2024 22:58:29 GMT  
		Size: 185.9 KB (185910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaa5c09573695eae4cc30eb4d47bc87fd4c1b52092a23b00dfac22e281e4a4a`  
		Last Modified: Thu, 08 Aug 2024 22:58:30 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6d12a9109e5f75da3d5b13f8f1bf9051aab77cb972a3d21b4b08423b79a548`  
		Last Modified: Thu, 08 Aug 2024 22:58:30 GMT  
		Size: 109.3 KB (109253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c813cfea7174c1c4281691b28917422832233ff6682cb0ec5011640779202d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ee5f00a41a5bcdeba8add1b05c558f179c6ccabb33b2974a6517a9c1124b1c`

```dockerfile
```

-	Layers:
	-	`sha256:46f7bc0330f336ecd6df6e5ed65eb42a0f05a44be0b96b0d088414a1cda2c764`  
		Last Modified: Thu, 08 Aug 2024 22:58:28 GMT  
		Size: 2.7 MB (2715728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4fa7546f0be6098118b92cb51652907a09d5b56ee7d9a1b4b3f2f20100b5bed`  
		Last Modified: Thu, 08 Aug 2024 22:58:28 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json
