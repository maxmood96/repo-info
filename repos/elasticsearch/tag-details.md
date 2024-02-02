<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.17`](#elasticsearch71717)
-	[`elasticsearch:8.12.0`](#elasticsearch8120)

## `elasticsearch:7.17.17`

```console
$ docker pull elasticsearch@sha256:f45c62e26c98be2bebecbd501429c2344118bf41d2a03dd528c78e9f50a211e7
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
$ docker pull elasticsearch@sha256:6ebdef574fb7a83dd4f21eb2f7c1b2cb61c7570a13add8254cef9da78a84cfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360385948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03598cf54b6466039d0f3c8526b4649cfc90ddbfc8872c97bd2b60d7d927291`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
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
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8267a6aaeba7c0ad2ae15343e114cb50dfdb25bde0232df9a69f6578cc0ec2a1`  
		Last Modified: Mon, 18 Dec 2023 19:53:16 GMT  
		Size: 7.3 MB (7327973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314340ae71fad54fe2bde96fe4b9ddf0ba484ab3aeb8d6c94a874a1074305cc4`  
		Last Modified: Mon, 18 Dec 2023 19:53:15 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ffe3636c39314dad879f9c08c6ef1fbe2d38dd1a1608fd7456ac8f23cbbe2f`  
		Last Modified: Tue, 23 Jan 2024 21:24:38 GMT  
		Size: 326.8 MB (326771934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6eb32f8fba7a82fe5a1190cbcf6e2167da41f5cd173f183b81d582eeead38af`  
		Last Modified: Tue, 23 Jan 2024 21:24:31 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54695f8a01f984a76b738a484e80f3cfe537d744d467db9345a48862831c88b2`  
		Last Modified: Tue, 23 Jan 2024 21:24:31 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a630bbcff66eedd8a2c0f766b32c0d6cf2759d1581ffb94c5e81f28885e0e4`  
		Last Modified: Tue, 23 Jan 2024 21:24:31 GMT  
		Size: 186.2 KB (186175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9381d05ac2de616366737c0c08d37d4db436229c019b7645c50ff5497745826c`  
		Last Modified: Tue, 23 Jan 2024 21:24:32 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f9f6db1acfc9a935add1bd942482aa81d5c3ab8c09c32bc489e0943fbda834`  
		Last Modified: Tue, 23 Jan 2024 21:24:32 GMT  
		Size: 109.3 KB (109254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.17` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0fb1d3b4a218d155979a29ebf3f194c2f267f6af9d020d4d93f217ba7aae83c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2107598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f8f30ff078e889601a7841a195aaf60f06edd687a624679a35a3aee37b4f3d`

```dockerfile
```

-	Layers:
	-	`sha256:451a606afc142274d72babf049f32cfd63f07265ad95eadbbfa0551f553e5cca`  
		Last Modified: Tue, 23 Jan 2024 21:24:31 GMT  
		Size: 2.1 MB (2069852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e6c6664a1ff9afd855b8ffcf607d4aef13205c90975c7ccbf1a967e0451f7b`  
		Last Modified: Tue, 23 Jan 2024 21:24:31 GMT  
		Size: 37.7 KB (37746 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.12.0`

```console
$ docker pull elasticsearch@sha256:60babaef216bd7af4cfa9784aec98b9336628fc2d859e40a89a9c1d617aee35f
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
$ docker pull elasticsearch@sha256:8d679e3a9e9bb8147bc723952c869043a7cacadd864a9b70b5aa03a7ef123cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.6 MB (456553538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c7be44706d939c595090b31091af233113acfcf875d5fbf99d8284eb666d53`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
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
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51be98b1d6e32cc22228ec68b71e2945257970e71f3a550061a4abecd4492d29`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 7.3 MB (7328019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7cc25a9ed6ca506a18bf041b668a08ef9a82e1c729ffb8271bba1b89a972e0`  
		Last Modified: Mon, 18 Dec 2023 19:52:19 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d091b041a789776af7adba81d26c6efbc74f9a4d2ad4bc282d7899a907e276fd`  
		Last Modified: Thu, 18 Jan 2024 21:43:44 GMT  
		Size: 422.9 MB (422939990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377d76c21e6adb4dc1fd4c625bd8ebf04434dfb707c6746641d8c2461edadd2e`  
		Last Modified: Thu, 18 Jan 2024 21:43:35 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a26d3f8b9182d47cb56cc4744b10be8488804df9c4bc63a739e6b87c9ce53f`  
		Last Modified: Thu, 18 Jan 2024 21:43:36 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb70a37b34d31a60c1099ab434464b52858ce81a0d4747b7f0e4e409eedc67b`  
		Last Modified: Thu, 18 Jan 2024 21:43:36 GMT  
		Size: 185.9 KB (185914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a75caff16ae8b7df99372f287b8f565c289c0e0130fa9c388a41393b491b85`  
		Last Modified: Thu, 18 Jan 2024 21:43:37 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264d475555cdb858fc449a1f14a576fefea236a224e0b115aba46b96636d9f65`  
		Last Modified: Thu, 18 Jan 2024 21:43:37 GMT  
		Size: 109.3 KB (109257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.12.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c3ed85e02cbf1d2696b10e87f30d8e67a5b08820f4220c2f29c8c04a6e9e6b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c57b4375682decd855049c97a70cb3aaf1132d00fb46d0e34d7ff8dd157fcf5`

```dockerfile
```

-	Layers:
	-	`sha256:6fe8d46232747704b92c860621c53724478b96131fb3acdf65df938cc63ed39f`  
		Last Modified: Thu, 18 Jan 2024 21:43:36 GMT  
		Size: 2.3 MB (2343114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a989a80f955ac24c0a80a695895b0ce328ddbe382849c566dfdc51fd43509449`  
		Last Modified: Thu, 18 Jan 2024 21:43:35 GMT  
		Size: 37.6 KB (37601 bytes)  
		MIME: application/vnd.in-toto+json
