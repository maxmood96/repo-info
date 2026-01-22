<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.10`](#elasticsearch81910)
-	[`elasticsearch:9.1.10`](#elasticsearch9110)
-	[`elasticsearch:9.2.4`](#elasticsearch924)

## `elasticsearch:8.19.10`

```console
$ docker pull elasticsearch@sha256:c874f965dd6fac82e185f871bbeaa1a51d65e2e6b97d71fe3201dfdd242fa77f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9e5d1d7fa7928bcbc1c16a6a51064d83aa13b0ee2e269366fb44408c118afddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.0 MB (710000547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0227f6f66638aad46c53e85299e287b091b2d9ef78ff9a2da837fdf9c4c0ff28`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:20:52 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 15 Jan 2026 22:20:52 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 15 Jan 2026 22:20:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:20:52 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 15 Jan 2026 22:22:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 15 Jan 2026 22:22:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 15 Jan 2026 22:22:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:22:26 GMT
ENV SHELL=/bin/bash
# Thu, 15 Jan 2026 22:22:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:22:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 15 Jan 2026 22:22:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 15 Jan 2026 22:22:27 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 15 Jan 2026 22:22:27 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 15 Jan 2026 22:22:27 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:49.939644068Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=493241b351be6d9f40d52a1406c91a23b4148821 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T22:07:49.939644068Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=493241b351be6d9f40d52a1406c91a23b4148821 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Thu, 15 Jan 2026 22:22:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:22:27 GMT
CMD ["eswrapper"]
# Thu, 15 Jan 2026 22:22:27 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c03eb992d21b08630d8ac503049a8718241ad97aa496f65e86ef83ecc4c9fda`  
		Last Modified: Thu, 15 Jan 2026 22:23:37 GMT  
		Size: 4.5 MB (4493983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80192c435f327724f0c26bc4cb00017e19aa75844ed49a17bbabbf1b5a144ada`  
		Last Modified: Thu, 15 Jan 2026 22:23:37 GMT  
		Size: 3.5 KB (3525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129766b9837a8a879dccafbe827bc492df6ba46b5db573a26bc6dbc9a819ce9`  
		Last Modified: Thu, 15 Jan 2026 22:23:31 GMT  
		Size: 675.5 MB (675485875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f857c18cb177c30c3e7cc8702c6d04273239f4c80660f2ea9eca9a1b55a6376`  
		Last Modified: Thu, 15 Jan 2026 22:23:19 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba08e04d847400c4c6f3bc7d61f5580811f6a37a8e5ad5b79179b73883072447`  
		Last Modified: Thu, 15 Jan 2026 22:23:20 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72d8b944558d4ac06b4eac8fb20864bcc70746e2c9132d8fb6079f0afc3498`  
		Last Modified: Thu, 15 Jan 2026 22:23:40 GMT  
		Size: 163.9 KB (163938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acdd356e40bdedc39ff6be28c27c0f23c3603600e03721f26f3cb50e1d7d2bb`  
		Last Modified: Thu, 15 Jan 2026 22:23:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c906ecd5f0ac59a48c57178aa8bda7a96462366fa3e6add01bf6f32bdc41fd3`  
		Last Modified: Thu, 15 Jan 2026 22:23:21 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ab2210830ccfe04411aea858c47ae8ae0b3dacb9e1f0ad9449120d390d5805e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac7d496b691da1d07c5dd85de3d34cc7f7dceb9140fc5bcb7adc7f07020969c`

```dockerfile
```

-	Layers:
	-	`sha256:a8b98cb8971682b716b25524ec20fea3f4ee4a4b930dfc324a22a10b4649b519`  
		Last Modified: Fri, 16 Jan 2026 01:26:32 GMT  
		Size: 3.2 MB (3210136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d72ff81f2cafdf8acc84318265f241bcf9ce95f7eb02a9b2b268bf4f5baf670`  
		Last Modified: Thu, 15 Jan 2026 22:23:19 GMT  
		Size: 36.8 KB (36847 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:dce6afcf35b7496c9256f3b96bb70c45884bbbe265ee00679e21698a3ec274fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.8 MB (557805676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e39a33aefe5fb61bcacd1bdbf795f95890678c53414afb221679b6910731fa5`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:22:28 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 15 Jan 2026 22:22:29 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 15 Jan 2026 22:22:29 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:22:29 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 15 Jan 2026 22:23:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:23:34 GMT
ENV SHELL=/bin/bash
# Thu, 15 Jan 2026 22:23:34 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 15 Jan 2026 22:23:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 15 Jan 2026 22:23:34 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:49.939644068Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=493241b351be6d9f40d52a1406c91a23b4148821 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T22:07:49.939644068Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=493241b351be6d9f40d52a1406c91a23b4148821 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Thu, 15 Jan 2026 22:23:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:23:34 GMT
CMD ["eswrapper"]
# Thu, 15 Jan 2026 22:23:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cecb70ace38b5cdee15860059283a295171284116b721c39afdd3955e94530`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 4.5 MB (4498888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e4f5581ba049194157cd8d6ab4e92232b4aadb1ae418aafe5ba0de22bfe8b`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 3.5 KB (3524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e8ebd0db0bab4c12e2ef0315c656b022253aba7d11a10db6bcff83aab6658a`  
		Last Modified: Thu, 15 Jan 2026 22:24:21 GMT  
		Size: 524.2 MB (524152275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139356fa507a6e45e98749dcefde6b35c512077019929d5f71d22de5b562bcfb`  
		Last Modified: Thu, 15 Jan 2026 22:24:28 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ff06542254a202e810d0bb4e785ba6109267574b5b49db0471f1e0990d51af`  
		Last Modified: Thu, 15 Jan 2026 22:24:28 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e6a44bee32fbf11cd824cfb3c864c868121d59824f2cf524186a410d7a2e3e`  
		Last Modified: Thu, 15 Jan 2026 22:24:28 GMT  
		Size: 160.4 KB (160371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8303504bec948635617643b12f7cddc08d918a5db8e0e02352ace66e58b26062`  
		Last Modified: Thu, 15 Jan 2026 22:24:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f173cb2734f3479d8b874acef3ad9bee91b002aea67b734ef29c5d8b3295037`  
		Last Modified: Thu, 15 Jan 2026 22:24:28 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4a6b755816aced0923a319b912ed26259d366b246d69a16850424c1aaa8713fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3247599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e086ba01be4ec42db4ce99886c1232e2d33e3e84750443b7440a4a6b3b6013fe`

```dockerfile
```

-	Layers:
	-	`sha256:c98a7e76e13f71ef00ae7629b1061502a5b1865e1915ab46cb78065798e26714`  
		Last Modified: Fri, 16 Jan 2026 01:26:37 GMT  
		Size: 3.2 MB (3210549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ac5a82768f0b4690c0738d180d0bf35de57e76fe7b0c62aa0fdd64c37857f1`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 37.0 KB (37050 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.10`

```console
$ docker pull elasticsearch@sha256:e00900f6164b4c3a4240fb6893da7676e3d064b37f123fc8cbf31aba9bf6aae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0efd9b10af8d2f9ccfe3362d7728c0ea748c28eea110658b1b3243fadb3d59da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.7 MB (730670527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a7056347226d9bec0f7237e5625f1a107d5969e07d94d0fac99fc21eb5edba`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:14:30 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:14:30 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 20 Jan 2026 19:15:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:15:50 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 20 Jan 2026 19:15:50 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 20 Jan 2026 19:16:00 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 20 Jan 2026 19:16:00 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 20 Jan 2026 19:16:00 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:16:00 GMT
ENV SHELL=/bin/bash
# Tue, 20 Jan 2026 19:16:00 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:16:01 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 20 Jan 2026 19:16:01 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 20 Jan 2026 19:16:01 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 20 Jan 2026 19:16:01 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 20 Jan 2026 19:16:01 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 20 Jan 2026 19:16:01 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:16:01 GMT
CMD ["eswrapper"]
# Tue, 20 Jan 2026 19:16:01 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a026a888612da23815975bca8c84710416cf249b5988f7e16186f0f10c01d2`  
		Last Modified: Tue, 20 Jan 2026 19:17:16 GMT  
		Size: 4.3 MB (4285591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab04631026b3ad075947b117dcfee44500da4b95d729e73bb9d2c7072736aff`  
		Last Modified: Tue, 20 Jan 2026 19:16:53 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe00d3ed4551ee8cfa1166a0390c7e3be4ca65ada14090ec71ed785a6566985`  
		Last Modified: Tue, 20 Jan 2026 19:17:15 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db91f689250fc9486a38335862cfc1a01693fff341909f4d958882b89d73e97`  
		Last Modified: Tue, 20 Jan 2026 19:17:09 GMT  
		Size: 686.3 MB (686261769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d73e1ecddb45508e9ec41a52d7fbfeb225993becf3098b348c6a739b8dc3d4`  
		Last Modified: Tue, 20 Jan 2026 19:17:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a83a26879c155ed8e491397f0890d79a578247cfd9803de3342511a02a35c1`  
		Last Modified: Tue, 20 Jan 2026 19:17:15 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57640ded2f456cefbe2dc7e41caba0f5bef8b8c5223180a750b14936ff7b8d2`  
		Last Modified: Tue, 20 Jan 2026 19:16:54 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c6f1431793ab1a2b8c1ae82b4219742cd7d83ccc5b757db43479b39bbda43a`  
		Last Modified: Tue, 20 Jan 2026 19:16:55 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:da920b28f103a2153b6144483c794c659a2132580bc34fc60d6fe694166fc7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe88e30dcc468e785f9716cb239c64abb304f2cded2657f9a25d6791aa67fc3`

```dockerfile
```

-	Layers:
	-	`sha256:ac0ba00d918a2d81d661b8ce7e9845b6b3b771bb123a372b6d0461743b3b69c2`  
		Last Modified: Tue, 20 Jan 2026 19:16:53 GMT  
		Size: 2.1 MB (2085724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e5585439e97a67b84d84f2e0e33984ba3c3e4163764566569b44f7ddddcbcb`  
		Last Modified: Tue, 20 Jan 2026 19:16:53 GMT  
		Size: 33.9 KB (33867 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:fc2e30f5e6fb1b3cd673c9cf58de8944de6afc7cdd92150d6b0a3402cee4ebca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574618984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5d0e70377f2fe6c05dd1167bdb3e1ecdaadf0cabbbc9453d4845b4abc7510`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:56:35 GMT
ENV container oci
# Mon, 19 Jan 2026 00:56:36 GMT
COPY dir:d1a1d4e8d07e3fe5bb075a89525931e1e2ca1718af0db53956bd13b04036076a in /      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:56:36 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:19Z" "org.opencontainers.image.created"="2026-01-19T00:56:19Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:19Z
# Tue, 20 Jan 2026 19:15:02 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:15:02 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 20 Jan 2026 19:15:59 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:15:59 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 20 Jan 2026 19:16:00 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 20 Jan 2026 19:16:06 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 20 Jan 2026 19:16:06 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 20 Jan 2026 19:16:06 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:16:06 GMT
ENV SHELL=/bin/bash
# Tue, 20 Jan 2026 19:16:06 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:16:06 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 20 Jan 2026 19:16:06 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 20 Jan 2026 19:16:06 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 20 Jan 2026 19:16:06 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 20 Jan 2026 19:16:06 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 20 Jan 2026 19:16:06 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:16:06 GMT
CMD ["eswrapper"]
# Tue, 20 Jan 2026 19:16:06 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461f8e8d97b13153665b3c17a7a281e397de107af04a6d62cb1dd9ea9390ee0f`  
		Last Modified: Tue, 20 Jan 2026 19:16:45 GMT  
		Size: 4.3 MB (4301521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254580abb5e1c4dea6b8884140bcdadfdefc8b4464914bd27ef7ffccc4db677d`  
		Last Modified: Tue, 20 Jan 2026 19:16:58 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef44ddcad081bdc44e1acef18085fb0424f640ab90d4162d4f4f755917ed62df`  
		Last Modified: Tue, 20 Jan 2026 19:16:45 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dde05b1038ddcb474acb82be42b5df4f90d932af980e582fc281ac556426aa`  
		Last Modified: Tue, 20 Jan 2026 19:42:36 GMT  
		Size: 532.0 MB (532020333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e19fd42fb3086611fb5f4cbf9d1246cb3e86462a3a574421fc2ee8d23fd7e80`  
		Last Modified: Tue, 20 Jan 2026 19:16:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218624e1fd7111cb79d9ef34c1d9d9c006a8479cc2e0f404c4351361bef1879c`  
		Last Modified: Tue, 20 Jan 2026 19:16:46 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e525deb51862836c57f22a26e0ba1bfc472f709aab296956337056d6d7e8645`  
		Last Modified: Tue, 20 Jan 2026 19:16:46 GMT  
		Size: 74.1 KB (74109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cd04ab6f59c40fefccc8f3b32b0fc800ab6e6fbfbc8e74f85d0c00d00b735c`  
		Last Modified: Tue, 20 Jan 2026 19:16:47 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f4043f05cd836b1516626a768befc8218831a8866b5cba9f015350eaf3ad477f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fe7b562f593735e658be8de5f23731cc37ab824c637f9e7381eefdd954c049`

```dockerfile
```

-	Layers:
	-	`sha256:b79dacaa4d0a80248c269780a47cb4ad11ae946b7536f451c490a243f626259d`  
		Last Modified: Tue, 20 Jan 2026 22:25:28 GMT  
		Size: 2.1 MB (2086286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0b9f56f1ee14398685a15ebfcde3eab644fd47609221facd7ab0eaa34052b2`  
		Last Modified: Tue, 20 Jan 2026 22:25:31 GMT  
		Size: 34.0 KB (34049 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.4`

```console
$ docker pull elasticsearch@sha256:e40ae5dc1e03bb8f5d30ee2491e39629b5d5ef51f7a069fe3de177fe2a09a70e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b81a3b97a355e441873876de1ce705c151a3acf900e8728af5136d3116e94bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 MB (738206758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58584621d40620fd527c3d6a8a52cae42bf39dc5dc275194ecd5a5219c4129`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:15:39 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:15:39 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:16:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 20 Jan 2026 19:16:52 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 20 Jan 2026 19:17:02 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 20 Jan 2026 19:17:02 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 20 Jan 2026 19:17:02 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:17:02 GMT
ENV SHELL=/bin/bash
# Tue, 20 Jan 2026 19:17:02 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:17:02 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 20 Jan 2026 19:17:02 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 20 Jan 2026 19:17:02 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:25.170027027Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dfc5c38614c29a598e132c035b66160d3d350894 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T22:07:25.170027027Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dfc5c38614c29a598e132c035b66160d3d350894 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 20 Jan 2026 19:17:02 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 20 Jan 2026 19:17:02 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 20 Jan 2026 19:17:02 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:17:02 GMT
CMD ["eswrapper"]
# Tue, 20 Jan 2026 19:17:02 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3222a9398147341da87995bf6de70586c43a09be5dca4c8fe5ef9361e3f795f`  
		Last Modified: Tue, 20 Jan 2026 19:17:55 GMT  
		Size: 4.3 MB (4285542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437e14bfbd8d773e97274067d1174a780f045b6cdd8494ec254396b5de779f8f`  
		Last Modified: Tue, 20 Jan 2026 19:18:14 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2948a5c8a11588090a3334781ed6fc0bcfe1688e405f3cec79d97f87842a7a4c`  
		Last Modified: Tue, 20 Jan 2026 19:17:55 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c0a9144959b9bde6d97dd65501f32df6fcde7429eb21ee700b9124eb9d037`  
		Last Modified: Tue, 20 Jan 2026 19:18:10 GMT  
		Size: 693.8 MB (693798050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b1cb20601ad7645009d39243042369152b9832f7d1ce35ad603a22d773c5be`  
		Last Modified: Tue, 20 Jan 2026 19:17:56 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f818b3a8dfd805855db34e2bdff3a1e81758f0371a2820648a09a764d44f08`  
		Last Modified: Tue, 20 Jan 2026 19:17:56 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a78aba10dfda2f39fc889b9f4a70705ff5dca9995bbabde1264bd84402b464`  
		Last Modified: Tue, 20 Jan 2026 21:14:33 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23be4bf5d6c4cd7e6c4cf205b6ec7eed5237a38d3bbdfadeb4026a995a24951`  
		Last Modified: Tue, 20 Jan 2026 19:18:14 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6968544519fd904f6ba3c731fbca0e6ff9f74e2dea360f6ffb4deaf0c554159e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ec41daf9acb5c37f3edff37ee16d6cbbe892bf444c4fb0f53edcc533eee0f7`

```dockerfile
```

-	Layers:
	-	`sha256:08d5696b1ccf27193eaba573e3bfc8a8ad01e60b7d8b3525f4fdca6ad578660b`  
		Last Modified: Tue, 20 Jan 2026 22:25:32 GMT  
		Size: 2.1 MB (2098083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8556a8cf7779e87838db56e1e9e299cbed983390f315a3cfb1806b14e8997f`  
		Last Modified: Tue, 20 Jan 2026 19:17:55 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:82beab757ad2d4d960bce7541eecbfecb252cc933a99330a8aa044c7829a79b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.2 MB (582182424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00550e06668981860c1a7d0029133f98fa72e445eb04750246920b47e7b63e8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:56:35 GMT
ENV container oci
# Mon, 19 Jan 2026 00:56:36 GMT
COPY dir:d1a1d4e8d07e3fe5bb075a89525931e1e2ca1718af0db53956bd13b04036076a in /      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:56:36 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:19Z" "org.opencontainers.image.created"="2026-01-19T00:56:19Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:19Z
# Tue, 20 Jan 2026 19:14:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:14:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 20 Jan 2026 19:15:53 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:15:53 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 20 Jan 2026 19:15:53 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 20 Jan 2026 19:15:59 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 20 Jan 2026 19:15:59 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 20 Jan 2026 19:15:59 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:15:59 GMT
ENV SHELL=/bin/bash
# Tue, 20 Jan 2026 19:15:59 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:15:59 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 20 Jan 2026 19:15:59 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 20 Jan 2026 19:15:59 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:25.170027027Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dfc5c38614c29a598e132c035b66160d3d350894 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T22:07:25.170027027Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dfc5c38614c29a598e132c035b66160d3d350894 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 20 Jan 2026 19:15:59 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 20 Jan 2026 19:15:59 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 20 Jan 2026 19:15:59 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 20 Jan 2026 19:15:59 GMT
CMD ["eswrapper"]
# Tue, 20 Jan 2026 19:15:59 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e466c7d96095fc16dda06a339f057680e50fe6e65aa5254be9e932af2a746328`  
		Last Modified: Tue, 20 Jan 2026 19:16:58 GMT  
		Size: 4.3 MB (4301519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f048a3aa29eff2b6c093af2ab0dc91b1a81beee9f11ba5b5a68300e706172b92`  
		Last Modified: Tue, 20 Jan 2026 21:11:57 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f128170a04d98566ea0f7eea1db71ec0600414f0c1f7b790aa96d8e11d3b83b7`  
		Last Modified: Tue, 20 Jan 2026 19:16:38 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5555ae7a3b0055ae28b9ad2e111f31e2e55d0972891889aa8f771fb094a0eac`  
		Last Modified: Tue, 20 Jan 2026 19:16:51 GMT  
		Size: 539.6 MB (539583776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb4be9efbf51cc3728d3838d60889b94f152b5150c4bf119142d4073611e4a0`  
		Last Modified: Tue, 20 Jan 2026 19:16:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d959e0746b4aacb24bad70c20322b60d9a20097df430b73a02252fd90ae9cb3c`  
		Last Modified: Tue, 20 Jan 2026 19:16:58 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e21fa1c522ab5440bec5d53980ef5cf91251b47e01b828067f2d04eaa12589`  
		Last Modified: Tue, 20 Jan 2026 22:45:19 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda189c13b5c3f6d611ac39be78bea0a6a11ceaba3eb378ba0bcccfbbc754806`  
		Last Modified: Tue, 20 Jan 2026 19:16:58 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:db44c1af8beca90c7df39bba6dc54a41d0b2167c5b3e97c39fe6323959e8ae03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff79133d9fbe5ee7929fb6e2ddff585248c866057d9ea7418083418c2d586db`

```dockerfile
```

-	Layers:
	-	`sha256:7b043949e9191a2e565fb65eb202107f86767e848ff52c779327c8a0d03b442a`  
		Last Modified: Tue, 20 Jan 2026 19:16:39 GMT  
		Size: 2.1 MB (2098645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd05d3c33e9eedd44c065c1311c4494b3f6f2ddc467ffc05fa4fff1337a63c1c`  
		Last Modified: Tue, 20 Jan 2026 19:16:38 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json
