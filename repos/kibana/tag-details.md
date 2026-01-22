<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.10`](#kibana81910)
-	[`kibana:9.1.10`](#kibana9110)
-	[`kibana:9.2.4`](#kibana924)

## `kibana:8.19.10`

```console
$ docker pull kibana@sha256:bf71bccbd2e96858ef3e3a3551525f15c58a82ccb2f52b212b57a27bd8db86f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.10` - linux; amd64

```console
$ docker pull kibana@sha256:f4b33a8e7fd4eb7f30eef99f88ac7a6282859c6fa22c5cfcc376b5c62f82ad4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440929098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca95ea32292e68f944fc1f720bcec99d1b1927aa84f02a0f1d8930fa0588930`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Thu, 15 Jan 2026 22:30:02 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 15 Jan 2026 22:30:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 15 Jan 2026 22:39:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 15 Jan 2026 22:39:11 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 15 Jan 2026 22:39:11 GMT
RUN fc-cache -v # buildkit
# Thu, 15 Jan 2026 22:39:12 GMT
WORKDIR /usr/share/kibana
# Thu, 15 Jan 2026 22:39:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 15 Jan 2026 22:39:12 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:39:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:39:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 15 Jan 2026 22:39:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:39:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 15 Jan 2026 22:39:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 15 Jan 2026 22:39:13 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 15 Jan 2026 22:39:13 GMT
LABEL org.label-schema.build-date=2026-01-08T21:22:46.611Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6803805478ed373f560b161907994536f4cafef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T21:22:46.611Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6803805478ed373f560b161907994536f4cafef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Thu, 15 Jan 2026 22:39:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 15 Jan 2026 22:39:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 15 Jan 2026 22:39:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b1eabffcf7cbabe97a8f0016c86be2ac1d535d52d736cf34e226593c747b01`  
		Last Modified: Thu, 15 Jan 2026 22:40:25 GMT  
		Size: 9.4 MB (9432839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df8894e55e4556970e2b9bf6cf72ea85f6d82eaebcb74ae68f3299988e4874d`  
		Last Modified: Thu, 15 Jan 2026 22:40:31 GMT  
		Size: 385.1 MB (385126540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0d262662be73d762250fd3c2400cd7958731a423bca2ee83a3f0752e407b0`  
		Last Modified: Thu, 15 Jan 2026 22:40:24 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394fc48460e8e9bd15a1ce9c21b1367d22fef97ffad22607d06e75889dd6a38c`  
		Last Modified: Thu, 15 Jan 2026 22:40:11 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a83e2245c5d01687d265da75877f4722e2fe4be011920202354e1bd40ad60`  
		Last Modified: Thu, 15 Jan 2026 22:40:11 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b313b0b17fa53a6d9ed040fafecf22a537028112ae1952909a73999a4b05f`  
		Last Modified: Thu, 15 Jan 2026 22:40:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f7b2e3ea6526dc72585701719671110d7fd61dc1678490d714f43be08cac2`  
		Last Modified: Thu, 15 Jan 2026 22:40:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e68716b1b22fcbcace10fdb78c4bdec3450acca092a5bd016e56fd4d3db519`  
		Last Modified: Thu, 15 Jan 2026 22:40:13 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7286720fc832551fb7f047b4cf3a8ee99c374502cd2fee9790d2341749e30bcb`  
		Last Modified: Thu, 15 Jan 2026 22:40:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f968c1d5590a23ca7714b49d9b70a67aa644a8bd0513d0d77ce4886b0d378189`  
		Last Modified: Thu, 15 Jan 2026 22:40:14 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe913104181aef359465723f7a012bffc86bef3e180f385161e056b42ec4fd2f`  
		Last Modified: Thu, 15 Jan 2026 22:40:14 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.10` - unknown; unknown

```console
$ docker pull kibana@sha256:ef8f5e9f4ca796ab3ba7839d4009764c157b22e412caed8e88ad715caf667fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8504a82c72e1afa4cf64f98c37750339201c91da5f2b7b6fd749276e306f1fde`

```dockerfile
```

-	Layers:
	-	`sha256:7fbc9a55c90ebfdc703ba76f5460e4ff0d928315da5e1adc33180f08d67d891f`  
		Last Modified: Fri, 16 Jan 2026 00:12:24 GMT  
		Size: 4.9 MB (4919875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3856f8ea789516324ab0673d664b191a96f0d9df206eb01452e0bcc83e837745`  
		Last Modified: Fri, 16 Jan 2026 00:12:24 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:452de348001cfc2f23cc586790ff2749cc7125c3056dafb79555290273cbb108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.8 MB (453802317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03063e4180f2cf2902b699f7c814a934f9d94afb2af3ad2aca4397c9a0c0caf1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Thu, 15 Jan 2026 22:32:19 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 15 Jan 2026 22:32:19 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:24 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 15 Jan 2026 22:39:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 15 Jan 2026 22:39:24 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 15 Jan 2026 22:39:25 GMT
RUN fc-cache -v # buildkit
# Thu, 15 Jan 2026 22:39:25 GMT
WORKDIR /usr/share/kibana
# Thu, 15 Jan 2026 22:39:25 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 15 Jan 2026 22:39:25 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 15 Jan 2026 22:39:25 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:39:25 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 15 Jan 2026 22:39:25 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:39:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 15 Jan 2026 22:39:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 15 Jan 2026 22:39:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 15 Jan 2026 22:39:27 GMT
LABEL org.label-schema.build-date=2026-01-08T21:22:46.611Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6803805478ed373f560b161907994536f4cafef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T21:22:46.611Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6803805478ed373f560b161907994536f4cafef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Thu, 15 Jan 2026 22:39:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 15 Jan 2026 22:39:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 15 Jan 2026 22:39:27 GMT
USER 1000
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887bfd3dab63c341235f2310b2f0de104cf47abe15582bee09a26ccf72825307`  
		Last Modified: Thu, 15 Jan 2026 22:40:31 GMT  
		Size: 9.4 MB (9446894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95bea82121def6f659e94a168b2d3578c3662639c2e0e1af1b3cb235a969a3a`  
		Last Modified: Thu, 15 Jan 2026 22:40:41 GMT  
		Size: 398.9 MB (398851773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5210a6c3df4e77c6c34960aa0340797469fa56f0310b088dcacacbec14fa9`  
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14628f389a87888aaeb6be660f76ce62b53dddd2cd716cf1379a1293d07802b6`  
		Last Modified: Thu, 15 Jan 2026 22:40:32 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72028896f066f6d60d9b854656007e083860d9b967b3682aea199a00e73a6a03`  
		Last Modified: Thu, 15 Jan 2026 22:40:32 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b74d011e8a721332c54a4e3c8cd487b4b0f6e8e942f1a684d1bc40d30ee36e5`  
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5305e0985e4f342be0b93aa061f961cf70b478bf36b6e5c4a6ea6438ac132834`  
		Last Modified: Thu, 15 Jan 2026 22:40:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e24a5e0e735c4bc25f47eda0d2ba23d3f2c1f65c0aaa79fe3af2f9ad463f1`  
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc412c57150973172620afc0ce27cd2c97ed3334a07d3f640876ec18ce7aee7`  
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0b8604c295f0186a8d0e7c9f1dc2d81a9e06b94ad9dddba049fb9ea7e43e19`  
		Last Modified: Thu, 15 Jan 2026 22:40:35 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969b63fbb1f9012c56ada40cdc108ee255a385042e4ed698beb3157c73adec32`  
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.10` - unknown; unknown

```console
$ docker pull kibana@sha256:d2c85daaf81dae2045477187b43b134177a5a9a78c47e5d65560ced09d445222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520622879dd47c5613ed5b45257408198692b37086186aaf92806bd07f527459`

```dockerfile
```

-	Layers:
	-	`sha256:fb06acf56a1fec661a63ef7561301831d91e4b0938a588cab5fee383f6d8e8f0`  
		Last Modified: Thu, 15 Jan 2026 22:40:31 GMT  
		Size: 4.9 MB (4920939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fa3317520fb95a4da8283c6f1a06b6f126b688e389139c3d715b46ba6c9019`  
		Last Modified: Fri, 16 Jan 2026 00:12:30 GMT  
		Size: 41.2 KB (41163 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.10`

```console
$ docker pull kibana@sha256:54486f2bb39762104bd4dbb30ca3dacbc23628339b7cc614ba066896081f0608
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.10` - linux; amd64

```console
$ docker pull kibana@sha256:ba01b4ceafdcfb9bfe9775e453f926ac1bb3e3e46af473c1f8f9c6f7438e5691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441410107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c370de25c0150d351060e54a7e73b23bd7e7c871cdce767702638a853ee53d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 20 Jan 2026 19:15:41 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 20 Jan 2026 19:15:41 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:24:38 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 20 Jan 2026 19:24:38 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 20 Jan 2026 19:24:38 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 20 Jan 2026 19:24:38 GMT
RUN fc-cache -v # buildkit
# Tue, 20 Jan 2026 19:24:38 GMT
WORKDIR /usr/share/kibana
# Tue, 20 Jan 2026 19:24:38 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 20 Jan 2026 19:24:38 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:24:38 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:24:38 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 20 Jan 2026 19:24:38 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:24:39 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 20 Jan 2026 19:24:40 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 20 Jan 2026 19:24:40 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 20 Jan 2026 19:24:40 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 20 Jan 2026 19:24:40 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 20 Jan 2026 19:24:40 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 20 Jan 2026 19:24:40 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 20 Jan 2026 19:24:40 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 20 Jan 2026 19:24:40 GMT
USER 1000
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0770e51c6dd7cf02347915dfecd000e44f7bda343382646c5307c8276561cdd`  
		Last Modified: Tue, 20 Jan 2026 19:25:53 GMT  
		Size: 19.5 MB (19531264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb96aaca184439899c966fcf2e503541e5353bddb9112bcca2c60efd5fbe9`  
		Last Modified: Tue, 20 Jan 2026 20:06:24 GMT  
		Size: 365.3 MB (365287414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82ed9914f8ce421bd992f4cbbce2d9d9f0eb9c50a662b1d6eb3c91268411da2`  
		Last Modified: Tue, 20 Jan 2026 19:25:35 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3dfacef26f66b8bcd3f5c1c8cce93f5f88f3282f4fc189f284015507fc7ad2`  
		Last Modified: Tue, 20 Jan 2026 19:25:55 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149388f15f43f08872e025a09a966c9b5cbe36b349e96ebcf3d07a86a598cabb`  
		Last Modified: Tue, 20 Jan 2026 19:25:37 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176fbaaefaf20c32c18553282a3004decfd7be4735a8d4a1bae576a24023c671`  
		Last Modified: Tue, 20 Jan 2026 19:25:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf833c38ae1eea1f32f11bd13fd78c9930c331a40b750b4bd1a9fc6fd23089d3`  
		Last Modified: Tue, 20 Jan 2026 19:25:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bbc516ca76524ea6638a0458b5cb6931c7bcede7e9abfc6a2e7f3ba909df64`  
		Last Modified: Tue, 20 Jan 2026 19:25:39 GMT  
		Size: 4.7 KB (4742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a53fc5ff46817c2a7fa112fb6d4f8a3701a1c623f7ace9584b77478d5aeb4a`  
		Last Modified: Tue, 20 Jan 2026 19:25:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c2b7fc988002e19f6499cfafe1944cd84069d4e45a726df5132e0d9e4ba73c`  
		Last Modified: Tue, 20 Jan 2026 19:25:40 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819039b0385781223048c2d7efecfffb60e40924b7d3bfd30d4d8e5d77385318`  
		Last Modified: Tue, 20 Jan 2026 19:25:51 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b801a66adb7cbc4c2e93364c0f93de8069a4ee932342fe46aeed0c131910e5a`  
		Last Modified: Tue, 20 Jan 2026 19:25:51 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:b3daa631e040052d88899065eb4d2488b1e5b80f95c54b9ea63922807ed865ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5718273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4376664d8c7595656b300d944e72d6b379f75c4c40b57810d73506d276d002`

```dockerfile
```

-	Layers:
	-	`sha256:d099f5ca3f1a990d59ac1af115193d2e1f79750c8175b0603f329e89d56131aa`  
		Last Modified: Tue, 20 Jan 2026 19:25:36 GMT  
		Size: 5.7 MB (5675040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f24a578175857ada7d3e146537f59a79be0c97c4c787173fe6fd65d4d00a08`  
		Last Modified: Tue, 20 Jan 2026 19:25:35 GMT  
		Size: 43.2 KB (43233 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2aec16a748598201269c7db5f95e4712f047bd9487d363d64147490ac73594d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453234328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada9326f147170ac0fc487550940822ac1aa3d880f5e06d9da08762cd87b319e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 20 Jan 2026 19:14:56 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 20 Jan 2026 19:14:56 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:22:20 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 20 Jan 2026 19:22:21 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 20 Jan 2026 19:22:21 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 20 Jan 2026 19:22:21 GMT
RUN fc-cache -v # buildkit
# Tue, 20 Jan 2026 19:22:21 GMT
WORKDIR /usr/share/kibana
# Tue, 20 Jan 2026 19:22:21 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 20 Jan 2026 19:22:21 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:22:21 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:22:21 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 20 Jan 2026 19:22:21 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:22:22 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 20 Jan 2026 19:22:23 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 20 Jan 2026 19:22:23 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 20 Jan 2026 19:22:23 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 20 Jan 2026 19:22:23 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 20 Jan 2026 19:22:23 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 20 Jan 2026 19:22:23 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 20 Jan 2026 19:22:23 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 20 Jan 2026 19:22:23 GMT
USER 1000
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1ce2c5dd2d035c09e88c00cfe052acda3da050181861289efe99919f26854`  
		Last Modified: Wed, 21 Jan 2026 03:58:48 GMT  
		Size: 19.5 MB (19482353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213e947701a25a6f3bf26ee6f55cf1db4a973abf7f7a2dac29b6cbef2bdd2f41`  
		Last Modified: Wed, 21 Jan 2026 03:58:59 GMT  
		Size: 379.0 MB (378986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a4b6c3ea8777a5a979fa9eccde77415ab344f0d2ffcc58c829150464007f8a`  
		Last Modified: Tue, 20 Jan 2026 19:23:26 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc28000f6f72466eb4bf4e12d06bd7a0b917ea15f80cda515a806d9ef32c21e4`  
		Last Modified: Tue, 20 Jan 2026 19:23:41 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723d86436e01078a570f6d99923adeebc956f258c5c7640ee511f1885f27cc5c`  
		Last Modified: Tue, 20 Jan 2026 19:23:38 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a47ed34feb4e8d221ff26d00a9cc3ab698c3112a5a32f9373e26e7eda060f5`  
		Last Modified: Tue, 20 Jan 2026 19:23:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7f9931fc4843c117493bf2c2d1a8de0d492f6c655ba29717688e05cd22467c`  
		Last Modified: Tue, 20 Jan 2026 19:23:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d856fd403aca50e8250d35be7203c17a853a5a54ce23185e92c40dd775a36c11`  
		Last Modified: Tue, 20 Jan 2026 21:18:14 GMT  
		Size: 4.7 KB (4738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3fbe5659f06b803192c8704929e430bfd2d1cb6e33d49b96c4f68317d3d463`  
		Last Modified: Tue, 20 Jan 2026 19:23:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e14956950be0772bf321e2cf85012845f9c4f63521d30e7e8849c69242b5419`  
		Last Modified: Tue, 20 Jan 2026 19:23:29 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c80fe6ad3901eec5c80f6e8363131ba0bba45f61501a2774d06e635c420c1a`  
		Last Modified: Tue, 20 Jan 2026 19:23:30 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46484fed8ecfcc765861fc956a46963feef62ef108cd6dfa1dd200eb472f5cdf`  
		Last Modified: Tue, 20 Jan 2026 21:18:16 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:d696894e18b10d42f00a2bb1e92886b9baefec04c39fbf17e46f9fe2872624a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea132aeefd5121c0dda22ab130ca2df55d720ec3d04a28fc2f62a7953d180b7`

```dockerfile
```

-	Layers:
	-	`sha256:5324ef9093b933bf6eeb5bd799def030a1276a83944302f4551c22ff1f2fa760`  
		Last Modified: Tue, 20 Jan 2026 19:23:27 GMT  
		Size: 5.7 MB (5673712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b3655f1385adcf8f16327743882c03229bf3526dd139288851c75ea46db1a0`  
		Last Modified: Tue, 20 Jan 2026 21:11:59 GMT  
		Size: 43.5 KB (43489 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.4`

```console
$ docker pull kibana@sha256:151deb5c481b2f61c05d1b267ee2066cf0700ed34fc323aeeebd5a4c0e5eb285
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.4` - linux; amd64

```console
$ docker pull kibana@sha256:9f2c8277f97b8b73bfa916415fc58db1f22f27cd611692b2415426b679412ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447470385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbb1f945416d9d08149831b80517f68480db596e69e24cefedc9bc4cfa6c59b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 20 Jan 2026 19:15:52 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 20 Jan 2026 19:15:52 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:25:10 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 20 Jan 2026 19:25:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 20 Jan 2026 19:25:11 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 20 Jan 2026 19:25:11 GMT
RUN fc-cache -v # buildkit
# Tue, 20 Jan 2026 19:25:11 GMT
WORKDIR /usr/share/kibana
# Tue, 20 Jan 2026 19:25:11 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 20 Jan 2026 19:25:11 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:25:11 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:25:11 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 20 Jan 2026 19:25:11 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:25:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 20 Jan 2026 19:25:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 20 Jan 2026 19:25:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 20 Jan 2026 19:25:13 GMT
LABEL org.label-schema.build-date=2026-01-08T21:40:45.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b05a85503d4590280c7e9263175269a5f4a09729 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T21:40:45.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b05a85503d4590280c7e9263175269a5f4a09729 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 20 Jan 2026 19:25:13 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 20 Jan 2026 19:25:13 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 20 Jan 2026 19:25:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 20 Jan 2026 19:25:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 20 Jan 2026 19:25:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6a69b10009198c74a2ac3b61415a09a06380ac7971feaaa634be9a37f35c3a`  
		Last Modified: Tue, 20 Jan 2026 19:26:30 GMT  
		Size: 19.5 MB (19531247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0601875ead284e90a33a9b440c3bac24be469adb8171ac8289789c74d719ea76`  
		Last Modified: Tue, 20 Jan 2026 19:26:19 GMT  
		Size: 371.3 MB (371347564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd54da4026c91c1318bdd2be7cbc6aff8ebeb532c24f4a56c4b8d3863723f87`  
		Last Modified: Tue, 20 Jan 2026 19:26:11 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dafc83e14f0589dfb3f2d4c7fe851b82199fcb67a2b3464f95ce91d2ad29f4f`  
		Last Modified: Tue, 20 Jan 2026 19:26:28 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9404a56198b93a3d70a5b782d52ba2f70ed9d8a44ff296036dae903dd75bf674`  
		Last Modified: Tue, 20 Jan 2026 19:26:12 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bcfdbf865a1807deaa0be6be00d1e4a0f3f931b01eacebb990d3aa0368b5d1`  
		Last Modified: Tue, 20 Jan 2026 19:26:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced885a781da9f9781cdbce3b562750cf88789eed1f4604eaaa85a7af31151c8`  
		Last Modified: Tue, 20 Jan 2026 19:26:25 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c698c799ec5aa6f8a8733ff412fc1634cac6b3a7501c7d98d873c0a95967e41e`  
		Last Modified: Tue, 20 Jan 2026 19:26:14 GMT  
		Size: 4.9 KB (4891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396b851127f2fd99e5a74fad07cd12599732438163b1d10b76ab1d4831c1e01c`  
		Last Modified: Tue, 20 Jan 2026 19:26:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd15e7d9fc2df424bcc4154120667fa04cbdfcaecd5f4ef7cb5e265bc837ecad`  
		Last Modified: Tue, 20 Jan 2026 19:26:25 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e3a0692f5247566cfe41829b97717adb1fae7a00c4fb5c600349dc05442a57`  
		Last Modified: Tue, 20 Jan 2026 19:26:25 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a4aa8a194a49508286c20a2ccbfb081dbdb194017c6e016fc250a0ce6f5bdb`  
		Last Modified: Tue, 20 Jan 2026 19:26:16 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.4` - unknown; unknown

```console
$ docker pull kibana@sha256:03f89315bc464ab571d1a9f4accc00359ce04675fb6ef4b7b5182ba26a9d1866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e4df30f308148dbc5e03df2ebfb6cf8f11763a0d161a7ff68719f28840c9ee`

```dockerfile
```

-	Layers:
	-	`sha256:47e91ce357db4b5d320d8ea9524b54783f0968220110ecdd5db9f855852aa7d8`  
		Last Modified: Tue, 20 Jan 2026 19:26:12 GMT  
		Size: 5.8 MB (5750295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de522fbf6db0c5755b40b53a0422f8cd73566d3a2df1bf1c9153f474252253de`  
		Last Modified: Tue, 20 Jan 2026 19:26:11 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:5f1a0f23201fb212bd9591894dc92bf35373ef889199f4bf1371852dcbf8a794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.3 MB (459349737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40bdb897437179ab9009be50bb31ac32830a630079b9dcaa92d6cfa4995b1ef`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 20 Jan 2026 19:16:21 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 20 Jan 2026 19:16:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:23:55 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 20 Jan 2026 19:23:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 20 Jan 2026 19:23:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 20 Jan 2026 19:23:56 GMT
RUN fc-cache -v # buildkit
# Tue, 20 Jan 2026 19:23:56 GMT
WORKDIR /usr/share/kibana
# Tue, 20 Jan 2026 19:23:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 20 Jan 2026 19:23:56 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 20 Jan 2026 19:23:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:23:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 20 Jan 2026 19:23:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 20 Jan 2026 19:23:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 20 Jan 2026 19:23:58 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 20 Jan 2026 19:23:58 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 20 Jan 2026 19:23:58 GMT
LABEL org.label-schema.build-date=2026-01-08T21:40:45.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b05a85503d4590280c7e9263175269a5f4a09729 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T21:40:45.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b05a85503d4590280c7e9263175269a5f4a09729 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 20 Jan 2026 19:23:58 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 20 Jan 2026 19:23:58 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 20 Jan 2026 19:23:58 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 20 Jan 2026 19:23:58 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 20 Jan 2026 19:23:58 GMT
USER 1000
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e702ddcaff8c6f41969de37a5c2c5c06a9c62ae58c6e304b9538dc1252afa84`  
		Last Modified: Tue, 20 Jan 2026 19:25:27 GMT  
		Size: 19.5 MB (19482115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46edb31ef19c120e77f140cbc391e667dc6705d033d3251c32bd51cff031953`  
		Last Modified: Tue, 20 Jan 2026 19:25:12 GMT  
		Size: 385.1 MB (385102076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ab4735e75372063546ea4a6fed37c0dfbe7d63407c61c864f4605dfa5ab18c`  
		Last Modified: Tue, 20 Jan 2026 19:25:02 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff62b328f93960cdbfcc207f967f81e3f336d34b6144e38dfcd3349999c832e`  
		Last Modified: Tue, 20 Jan 2026 19:25:03 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d809d639a268326b48df12ec3c23dbe48b751e210fe8ba113a4d52b7e965fb75`  
		Last Modified: Tue, 20 Jan 2026 19:25:22 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f00ccdff817bc393bf9106db3247163631655c76ccb9e8203a000c77be5dc`  
		Last Modified: Tue, 20 Jan 2026 19:25:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14174022365c6627fc8aee6ad0d8afdd5b745ab202cccc1e886f83f8e43a7021`  
		Last Modified: Tue, 20 Jan 2026 19:25:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c972f788f3ff4a8508439a7f2521402c649942f138e3202d7fe66dc7d47630`  
		Last Modified: Tue, 20 Jan 2026 19:25:22 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e346af3dd7936502451b217d2a301b5570de850709cb597753c4b1ae0c8285e`  
		Last Modified: Tue, 20 Jan 2026 19:25:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763af489e8d17c055309d2775d6c40a9225b61c4d02ef274f488278cdf2a9c80`  
		Last Modified: Tue, 20 Jan 2026 21:55:09 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a924276a0bd886482403e79835d956303f5cbc5908f79436610981ec827062d`  
		Last Modified: Tue, 20 Jan 2026 19:25:06 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea57349e576ff60e11709a9e8bf8244a7c584debe26303d8bf4f4e7f114e215`  
		Last Modified: Tue, 20 Jan 2026 19:25:07 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.4` - unknown; unknown

```console
$ docker pull kibana@sha256:e359989d63e552a39a2f36afd464f96fed4edcf7bb5a2a74a3219e179900fde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cc02f7a7ab8c5be8c2c4183de7169a61730a1b0498ef009eefeeef263c36db`

```dockerfile
```

-	Layers:
	-	`sha256:921f25bd63265ed021ae127a1558110fcdaee28f43df27e1779b019e146510ee`  
		Last Modified: Tue, 20 Jan 2026 21:11:35 GMT  
		Size: 5.7 MB (5748967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:febd0bc74990374a026063eafcf03fefbf39a51853a937b813434ceacad5c1bc`  
		Last Modified: Tue, 20 Jan 2026 21:11:36 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
