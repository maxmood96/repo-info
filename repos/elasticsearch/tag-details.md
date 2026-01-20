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
		Last Modified: Thu, 15 Jan 2026 22:23:19 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:23:51 GMT  
		Size: 675.5 MB (675485875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f857c18cb177c30c3e7cc8702c6d04273239f4c80660f2ea9eca9a1b55a6376`  
		Last Modified: Thu, 15 Jan 2026 22:23:37 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba08e04d847400c4c6f3bc7d61f5580811f6a37a8e5ad5b79179b73883072447`  
		Last Modified: Thu, 15 Jan 2026 22:23:37 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72d8b944558d4ac06b4eac8fb20864bcc70746e2c9132d8fb6079f0afc3498`  
		Last Modified: Thu, 15 Jan 2026 22:23:40 GMT  
		Size: 163.9 KB (163938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acdd356e40bdedc39ff6be28c27c0f23c3603600e03721f26f3cb50e1d7d2bb`  
		Last Modified: Thu, 15 Jan 2026 22:23:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c906ecd5f0ac59a48c57178aa8bda7a96462366fa3e6add01bf6f32bdc41fd3`  
		Last Modified: Thu, 15 Jan 2026 22:23:37 GMT  
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
		Last Modified: Fri, 16 Jan 2026 01:26:33 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cecb70ace38b5cdee15860059283a295171284116b721c39afdd3955e94530`  
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
		Size: 4.5 MB (4498888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e4f5581ba049194157cd8d6ab4e92232b4aadb1ae418aafe5ba0de22bfe8b`  
		Last Modified: Thu, 15 Jan 2026 22:24:28 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:24:12 GMT  
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
		Last Modified: Fri, 16 Jan 2026 01:26:37 GMT  
		Size: 37.0 KB (37050 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.10`

```console
$ docker pull elasticsearch@sha256:d3eee558a27908ecbab13abe2c7a2da3916d82dd72059bcd4fa30db047f9def3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:074cf8dbaf38c21d1c091ed9cd74e1e05e055b6ef5da03df238504f5061a45d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.7 MB (730679535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8c2e353225161ffd82f10fda527bb68b96d5e837557ee5952a95b98419f089`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Tue, 13 Jan 2026 19:04:49 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:04:49 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:05:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:39 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 13 Jan 2026 19:05:39 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 13 Jan 2026 19:05:39 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:05:39 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:05:39 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:05:39 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:05:39 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:05:39 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 13 Jan 2026 19:05:39 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 13 Jan 2026 19:05:40 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:05:40 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:05:40 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:05:40 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e23f2204869bf926ac63b7d410dad1857f33da172f2d98b2a0b7e94f868fd1`  
		Last Modified: Tue, 13 Jan 2026 19:07:03 GMT  
		Size: 4.3 MB (4286930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d8823ef737cc217b99af433fdbb9eef9c194d322de487ce0340bc0b70cb6d7`  
		Last Modified: Tue, 13 Jan 2026 19:06:33 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75ec7e84981720a5c06beea4be6d44c1d3597bbdc477fca5d82196def0bd877`  
		Last Modified: Tue, 13 Jan 2026 19:07:03 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d168b0c63937f5028b69536c9dbe05759a406bcb1abc0e011456df0983419e6`  
		Last Modified: Tue, 13 Jan 2026 19:06:45 GMT  
		Size: 686.3 MB (686261903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2746896185b691a6f8363079f29e59e070d5e040f6012d2951e82c4f5754f853`  
		Last Modified: Tue, 13 Jan 2026 19:07:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ae8f92750e63523f31551a2cbf8e9e89b5d0a27bd0c12a58e1bb2f9b56d4b9`  
		Last Modified: Tue, 13 Jan 2026 19:06:35 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720a7bf8671812088c8bb58cb7042c43c318fefee2b67cc357250bee552bc595`  
		Last Modified: Tue, 13 Jan 2026 19:07:06 GMT  
		Size: 75.2 KB (75174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847482ebfea8d6fd8dc6b69b0af54a29a0e51e7693612cdbb1d0d1e7fa0c1649`  
		Last Modified: Tue, 13 Jan 2026 19:07:04 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:de81f30410fe8e436f7ab9608c29acc2020ea5cb8c709dd732f35dbfd26bc6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2cf6f5f01e394064c2985f6277f4846e1452b50eb204369e900dd9d478fc28`

```dockerfile
```

-	Layers:
	-	`sha256:d6f23ae1086f0f56481ac7b89aa7b3f1b3f8997322f168621c803bec5186be7a`  
		Last Modified: Tue, 13 Jan 2026 22:25:28 GMT  
		Size: 2.1 MB (2085720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88dbbf076513e616497b9c8eee42b5fec44f7d082952dc4a9f501da89b71ac78`  
		Last Modified: Tue, 13 Jan 2026 22:25:29 GMT  
		Size: 33.9 KB (33867 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:82a9f9951003b0ca40133589139d48622c74e6770112353eb6cb14f64ae0fa14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574629696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89daa3df089b833e2d13533923cfa69661b6205f90300f8e5dd6e72a071708b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Tue, 13 Jan 2026 19:04:56 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:04:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:31 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:05:31 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:31 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:37 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:05:37 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:05:37 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:05:37 GMT
LABEL org.label-schema.build-date=2026-01-08T22:08:21.336552225Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f2e019bd8110088070638ca779ec1543188c0f43 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T22:08:21.336552225Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f2e019bd8110088070638ca779ec1543188c0f43 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 13 Jan 2026 19:05:37 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 13 Jan 2026 19:05:37 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:05:37 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:05:37 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:05:37 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6eef4c50ba658394d871753e7b16d95d7f180af70fccbe59fa16350651bcc`  
		Last Modified: Tue, 13 Jan 2026 19:06:17 GMT  
		Size: 4.3 MB (4298172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4feb70d22c28cfc93d2a7df5ca12d959674d39b229819900252d87fdb1ad0440`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4aae3348ff67dcfc867e74ba7d93521cf602cc522d0c2875042b12c9abb756`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68acb52bef2ef59ccb0ac066ffd86c1cffd791d6070b775b4cad2bf0812fbac2`  
		Last Modified: Tue, 13 Jan 2026 19:09:13 GMT  
		Size: 532.0 MB (532020251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95f0ffa6327b4db525da6f9ce76baff708ded8fbf0a177b858e544a470ff009`  
		Last Modified: Tue, 13 Jan 2026 19:06:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdce219363a9ec7b79cb90fb71fbe48bfedd3a356eff83ad75c95396b9988ec7`  
		Last Modified: Tue, 13 Jan 2026 19:06:18 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bb0c47193e805c92ab1b4d1243c0212768703043c1972cc20a8fb7cffe19c2`  
		Last Modified: Tue, 13 Jan 2026 19:06:18 GMT  
		Size: 74.1 KB (74106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2be888867fe7da31fcb8dde53d5a2e2068ef34d393b53da119cc63580ed4b86`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4d6447aa360331dfe80a8ac179608602e418af946d13b976f66b6f5e1c727ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa578bca94c87534691bcf84136de56f6acdd34289f971b0b0be7c03baddb1f`

```dockerfile
```

-	Layers:
	-	`sha256:73b67e6d459854eab823ce4a6def697f894a8529570195b7df38317bc63a49eb`  
		Last Modified: Tue, 13 Jan 2026 22:25:33 GMT  
		Size: 2.1 MB (2086282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fb87ab692b4926a4c9557dfd4794ce94f62843951d84be3d67fb67acd3b77a`  
		Last Modified: Tue, 13 Jan 2026 19:06:16 GMT  
		Size: 34.0 KB (34049 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.4`

```console
$ docker pull elasticsearch@sha256:0266542f69c89f877dda8d1c8eaa235a084c4bee66d8ae5e2e5b86c78e0217bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b0ff3e5e81f31d0ea45d7c02f4002f19e02bcf6fc18a97645db0c6186bb468f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.2 MB (738215790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae97915efe574b9ab24db5cdce51385478620ae42a5de980b44922f43c75049`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Tue, 13 Jan 2026 19:05:06 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:05:06 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:05:50 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:50 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:59 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:06:00 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:06:00 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:06:00 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:25.170027027Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dfc5c38614c29a598e132c035b66160d3d350894 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T22:07:25.170027027Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dfc5c38614c29a598e132c035b66160d3d350894 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 13 Jan 2026 19:06:00 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 13 Jan 2026 19:06:00 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:06:00 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:06:00 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:06:00 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a877ebc65964478715852678c19a87adf2ab3a229532447230dbd0f0f5f609ac`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 4.3 MB (4286917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d947b5843b56e1069a042d0f4426a1a1a5fd4f030fc4a25336d4ea6576074290`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60461ed3c7672bb78ac1791b2f7345c220f7a2e1b19e8ab5dc905ffb19e5b3cc`  
		Last Modified: Tue, 13 Jan 2026 19:06:53 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375691d4f0e7a9e37f85dc57f9b782d46bbf12923c2cf2738bc0151d40a18ec8`  
		Last Modified: Tue, 13 Jan 2026 19:07:06 GMT  
		Size: 693.8 MB (693798165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65259db570a20d0ebb6f10a1b8d98ed8c12cce2bbab01ee8be3c702e981c215`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff621a01d060747a9f4f930bb9988ccb23aab774158fdeef0f955250955e4b5f`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47daa5a9ab20e056fbf6ef84aa9d237f9223d0660fd3197b4821d4ca700830fe`  
		Last Modified: Tue, 13 Jan 2026 19:07:22 GMT  
		Size: 75.2 KB (75176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f457b6a3af683cddc209588fc640c8bebbf8df156bdf7fdaa3e4d8f474ba015`  
		Last Modified: Tue, 13 Jan 2026 19:06:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0fafd42043b2e56aa2f99b6a1f6be13e83d608f06b4d62d99036ecca190ef480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a78366f7f46241a909568f5764b41d83c9db9460c0d013424d027c3588e3dbf`

```dockerfile
```

-	Layers:
	-	`sha256:7b0b6ab2fffb9a4759bc08ca5d7d7984ee74be35ee8cee577a8b18e57b6d0590`  
		Last Modified: Tue, 13 Jan 2026 19:06:53 GMT  
		Size: 2.1 MB (2098079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0cb1f137ee81e81f96eeb4c570c8790867ec39dd88930b0f5485a0e286ad20`  
		Last Modified: Tue, 13 Jan 2026 22:25:39 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a3ea466801f0a1b488862a5ff7f2fc57618b110c81e9f3394b0dce53d24aca3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.2 MB (582193062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c9efd012faea1fdb6d2f3ea00158aac0b5ff8459270734fa4215db2e8b9df6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Tue, 13 Jan 2026 19:05:02 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:05:02 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 13 Jan 2026 19:05:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:05:35 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:05:35 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 13 Jan 2026 19:05:42 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:05:42 GMT
ENV SHELL=/bin/bash
# Tue, 13 Jan 2026 19:05:42 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 13 Jan 2026 19:05:42 GMT
LABEL org.label-schema.build-date=2026-01-08T22:07:25.170027027Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=dfc5c38614c29a598e132c035b66160d3d350894 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T22:07:25.170027027Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=dfc5c38614c29a598e132c035b66160d3d350894 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 13 Jan 2026 19:05:42 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 13 Jan 2026 19:05:42 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:05:42 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 19:05:42 GMT
CMD ["eswrapper"]
# Tue, 13 Jan 2026 19:05:42 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e62a8581c382d8da952c01546837d1fe0f5c11d5f5f6ef729eb63188fb7837`  
		Last Modified: Tue, 13 Jan 2026 19:06:23 GMT  
		Size: 4.3 MB (4298096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018848372f79ca08b0d1aba230bd8f3454483c4b2327a7c2b2fb91d2d82aea7f`  
		Last Modified: Tue, 13 Jan 2026 19:06:38 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dec0cfbb4bd918688e8dc322c026d75462b49ca7969fc8825aaf87583baa4c`  
		Last Modified: Tue, 13 Jan 2026 19:06:23 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc7abb11045518494838a2041f3c44ef5d8f27247b888f54fe76b6bd750cc4`  
		Last Modified: Tue, 13 Jan 2026 19:06:32 GMT  
		Size: 539.6 MB (539583697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963ad772b8813588b7843e9f65eea33c02aba4f4f6a1841f85b6065ed134aa05`  
		Last Modified: Tue, 13 Jan 2026 19:06:24 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4656c38f6aee475dde7362b44f7dcc8c8fe5e043cab002fb333067a69c81bfec`  
		Last Modified: Tue, 13 Jan 2026 19:06:24 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e9d27770b758c838e17a3240638a99e68743110bbac384f8d22399e30ab55`  
		Last Modified: Tue, 13 Jan 2026 19:06:39 GMT  
		Size: 74.1 KB (74104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c8d90ed27fef28cf3d1193c7ead1b4a5c08122ddcd03f12ecad40fc4b8bfc`  
		Last Modified: Tue, 13 Jan 2026 19:06:38 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:71598f08ef45f33ee8bfd84931a2cd741dcebbec81225fea1fbfb7ff43ec193a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e5501790c44a3ff757065de73ee9aaebdcd449299c2594bb8d096e2dab4d7c`

```dockerfile
```

-	Layers:
	-	`sha256:b751cb3303bcd07a4220c4a74c284b7f4703e7477c4878a4fdb7a765f4da5f60`  
		Last Modified: Tue, 13 Jan 2026 22:25:48 GMT  
		Size: 2.1 MB (2098641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcc8a775d50a2ffebe49f6603f38c1793debe5bf7a353f32c7e82863d54ac872`  
		Last Modified: Tue, 13 Jan 2026 22:25:48 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
