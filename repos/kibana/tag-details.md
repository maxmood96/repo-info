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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:40:10 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394fc48460e8e9bd15a1ce9c21b1367d22fef97ffad22607d06e75889dd6a38c`  
		Last Modified: Thu, 15 Jan 2026 22:40:11 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a83e2245c5d01687d265da75877f4722e2fe4be011920202354e1bd40ad60`  
		Last Modified: Thu, 15 Jan 2026 22:40:24 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b313b0b17fa53a6d9ed040fafecf22a537028112ae1952909a73999a4b05f`  
		Last Modified: Thu, 15 Jan 2026 22:40:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14f7b2e3ea6526dc72585701719671110d7fd61dc1678490d714f43be08cac2`  
		Last Modified: Thu, 15 Jan 2026 22:40:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e68716b1b22fcbcace10fdb78c4bdec3450acca092a5bd016e56fd4d3db519`  
		Last Modified: Thu, 15 Jan 2026 22:40:24 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7286720fc832551fb7f047b4cf3a8ee99c374502cd2fee9790d2341749e30bcb`  
		Last Modified: Thu, 15 Jan 2026 22:40:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f968c1d5590a23ca7714b49d9b70a67aa644a8bd0513d0d77ce4886b0d378189`  
		Last Modified: Thu, 15 Jan 2026 22:40:24 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe913104181aef359465723f7a012bffc86bef3e180f385161e056b42ec4fd2f`  
		Last Modified: Thu, 15 Jan 2026 22:40:24 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887bfd3dab63c341235f2310b2f0de104cf47abe15582bee09a26ccf72825307`  
		Last Modified: Thu, 15 Jan 2026 22:40:49 GMT  
		Size: 9.4 MB (9446894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95bea82121def6f659e94a168b2d3578c3662639c2e0e1af1b3cb235a969a3a`  
		Last Modified: Thu, 15 Jan 2026 22:40:57 GMT  
		Size: 398.9 MB (398851773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5210a6c3df4e77c6c34960aa0340797469fa56f0310b088dcacacbec14fa9`  
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14628f389a87888aaeb6be660f76ce62b53dddd2cd716cf1379a1293d07802b6`  
		Last Modified: Thu, 15 Jan 2026 22:40:49 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72028896f066f6d60d9b854656007e083860d9b967b3682aea199a00e73a6a03`  
		Last Modified: Thu, 15 Jan 2026 22:40:32 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b74d011e8a721332c54a4e3c8cd487b4b0f6e8e942f1a684d1bc40d30ee36e5`  
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5305e0985e4f342be0b93aa061f961cf70b478bf36b6e5c4a6ea6438ac132834`  
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:40:47 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969b63fbb1f9012c56ada40cdc108ee255a385042e4ed698beb3157c73adec32`  
		Last Modified: Thu, 15 Jan 2026 22:40:35 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:12:30 GMT  
		Size: 4.9 MB (4920939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7fa3317520fb95a4da8283c6f1a06b6f126b688e389139c3d715b46ba6c9019`  
		Last Modified: Fri, 16 Jan 2026 00:12:30 GMT  
		Size: 41.2 KB (41163 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.10`

```console
$ docker pull kibana@sha256:92659a0af9332fc3115b12348473709994cad579c1ed28f738b89ba3c45a77dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.10` - linux; amd64

```console
$ docker pull kibana@sha256:6d55ebef44242abc57476edd335c510ac16a905476d360f4a16969d4e23cd36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441416565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d22e7d6f23e07359059c8ae816b86370881039e07c02de18450eb49876791e7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 13 Jan 2026 19:05:15 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:05:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:13:45 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:13:46 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:13:46 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:13:46 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 13 Jan 2026 19:13:47 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 13 Jan 2026 19:13:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:13:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:13:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4bc21e5de8adf1269e10e4e48cbe203a2e5daf830d703e20e99172ae58857f`  
		Last Modified: Tue, 13 Jan 2026 19:14:42 GMT  
		Size: 19.5 MB (19530147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19903af0dde482fbc9576ed9d0a3df7d0b3d3b87a16c4ffbddaaf143307c35ca`  
		Last Modified: Tue, 13 Jan 2026 19:14:48 GMT  
		Size: 365.3 MB (365287415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913a81407a2be3a11cf45a191fd443cef612f508e51cf4e580bc76adbe1c636`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9446220ea6a418be5dc5754de5228ec08cca75eec99693ecdd0bd8f72fe9d8b7`  
		Last Modified: Tue, 13 Jan 2026 19:14:57 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a31fa8bab6b5b488e96f7a463584c15982a9d1270c48fde9e8a162ae87220`  
		Last Modified: Tue, 13 Jan 2026 19:14:42 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f274bc2c4e97f1aa92fe3ab520f6733ea75637bbc4721b4d32cad7efa5464025`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab827071fc434fb8ac3d65438c819e2dfedd2455ec2fce0157d49e8752bc1c2`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae69bf708487ae67a5591c54fb34bfcdba2c1ee8bcf9b564ec14f8152e62594`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 4.7 KB (4743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4298a6de0d2303414159d0e45b04257522121a47498fa5e77fc61daace04c35b`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c58ba0d8485a45c7aa910d161858535c638abb02c94d1d242e07e5887477671`  
		Last Modified: Tue, 13 Jan 2026 19:14:45 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b07e6c36b3fb4b13b9f849605db0f2635492d27ab113659a6944e3430cbc963`  
		Last Modified: Tue, 13 Jan 2026 19:14:45 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc30e68fdb557e7573a75e3be2d8282a2947127b87140cc2ab3a9e0ffdc170f`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:9cfa1faa6d75f88ddda33449be78da06466f049d137b3cf43b038fe0db65e373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5718269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78edb067b5bdaea1adefa46a43faec793e22cf394e5142c97fe6ad789d8c25f7`

```dockerfile
```

-	Layers:
	-	`sha256:f064fd63cca4731797d7ed3dce6d8ebf5dc57b1d280b0c5c37cc36d1bd5d7034`  
		Last Modified: Tue, 13 Jan 2026 21:11:36 GMT  
		Size: 5.7 MB (5675036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e9a427827af141920bee46a3c2b45bc6d92fc809ce6aadabf3873b8f3154d7`  
		Last Modified: Tue, 13 Jan 2026 19:14:41 GMT  
		Size: 43.2 KB (43233 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9dd0d5c27bbdf5592d3028ea46a41fef0b1cf2bd57f16b71eb7623f28e65a1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453245696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38861e4f4846a6fad4c30e75f05094ee76e8c9c659f7047f2f38d2d9791df779`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 13 Jan 2026 19:05:30 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:05:30 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:12:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:12:56 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:12:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:12:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:12:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:12:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:12:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:12:58 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:12:58 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 13 Jan 2026 19:12:58 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 13 Jan 2026 19:12:58 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:12:58 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:12:58 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:12:58 GMT
USER 1000
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e9c0dfdf5c8970a5c67c4c352a3ca8842ddff4d8adadb3f6fd4f9e227f399d`  
		Last Modified: Tue, 13 Jan 2026 19:14:22 GMT  
		Size: 19.5 MB (19479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0675f37826a3a24fe5ddf889f8116a9e64b57f2a39febe9f679364a4db6a56`  
		Last Modified: Tue, 13 Jan 2026 19:15:08 GMT  
		Size: 379.0 MB (378986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e645d82dbc194239a72b2b6fc213e8f887f5a79272358466f2a47f7c1ab5d1f`  
		Last Modified: Tue, 13 Jan 2026 19:14:17 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb44ba49a5b4b8418e4efc914345d8e2f3802952d6631f062a3609dd312ff25`  
		Last Modified: Tue, 13 Jan 2026 19:14:19 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518cad7b7c64e5232478f71730dd7c2f0c4e2e22db9f2ab4db237c0a477180fb`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662e6d71d830b9f06ca4ca97d6fae8f8e420737d8423cc5ca6812e48d02a25a1`  
		Last Modified: Tue, 13 Jan 2026 19:14:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1699c3a8ddb6e71e4775eee7dc931bbaed51b40eee9159141367c2edf10edf9`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206d6eea901e3724603a18076b288f1a6b89390b552422b7c0b3add60c26662`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 4.7 KB (4745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec7191dd7cc12a99ce9c07f5daaf537de54941c85d2eb594912c8ee3f4ce990`  
		Last Modified: Tue, 13 Jan 2026 19:14:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563e7d6683cac25caac1aa1562074e5dfd4225a3842c5a2a6be2bb58208c7947`  
		Last Modified: Tue, 13 Jan 2026 19:14:17 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4f2b4e45c56cfc16217574d813ca8aa904158bbdb679a00e319525baa100f9`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2958589136402310dc82339f43f0feec6756d724cb401c9f7d3efb2253b63c`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:61d741d2ecd5b0e12e98bb0ca281d255da83b8bc9a495160df31332b3ab22cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7558bbf2991c66fd0d9bbe704a6f0e21adaba7fdcfae8b01cd00ab0cc79ca9f4`

```dockerfile
```

-	Layers:
	-	`sha256:c16292918cdc0d579be52c52518b58131ea2dd51f30ef0e761e53df52ea91b0e`  
		Last Modified: Tue, 13 Jan 2026 21:11:43 GMT  
		Size: 5.7 MB (5673708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dccbbfa37d4996dc0bf057db73154801a5bb9949692ea2d515daeebcb89286b`  
		Last Modified: Tue, 13 Jan 2026 19:14:02 GMT  
		Size: 43.5 KB (43490 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.4`

```console
$ docker pull kibana@sha256:d2302b46ae4e582ae6db41e8943bf47dfef7c7dc337417ce6dadd51e82ec8b15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.4` - linux; amd64

```console
$ docker pull kibana@sha256:c87190bf981f204ece46a242b1364e77a7d1f590e7e8df235c1ddec7d9ac9ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447476824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f01d3cc1cbb7ce592a2e2eeecd147a89bc51a7db323385a53b8a424ffb35816`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 13 Jan 2026 19:05:49 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:05:49 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:15:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:15:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:15:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:15:04 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:15:05 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:15:05 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:15:05 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:15:05 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:15:05 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:15:05 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:15:05 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:15:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:15:07 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:15:07 GMT
LABEL org.label-schema.build-date=2026-01-08T21:40:45.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b05a85503d4590280c7e9263175269a5f4a09729 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T21:40:45.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b05a85503d4590280c7e9263175269a5f4a09729 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 13 Jan 2026 19:15:07 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 13 Jan 2026 19:15:07 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:15:07 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:15:07 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:15:07 GMT
USER 1000
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f15fa39de48b205531a45ca6d6cda8094d4a06a6502acfddc34895d0b2643c3`  
		Last Modified: Tue, 13 Jan 2026 19:16:25 GMT  
		Size: 19.5 MB (19530112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dc175bbdd032134742011038dc122a2f03b2e439bcd7c8bd91302ca8dade07`  
		Last Modified: Tue, 13 Jan 2026 19:16:30 GMT  
		Size: 371.3 MB (371347565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb1920e9b91be4482a4007ae49dfc49b2dab20c8e703446ac086944247291fc`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe27caa33b43e2ccdbdd0014afc01f7312bd84a29531de9e47b5c93199dfdc4`  
		Last Modified: Tue, 13 Jan 2026 19:16:22 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e13713225303673880e773df8bb6d666655cd9fa2806fdcf9981a0874c0f69a`  
		Last Modified: Tue, 13 Jan 2026 19:16:07 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec254fefde6ee4be8512701f842bc8c140c62de5a73b71e11f28a11c22727f7`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4ac14c149cf5d7c0efc5314780041166f670cece91bce6a985508fce24ae2f`  
		Last Modified: Tue, 13 Jan 2026 19:16:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17ac5dc97322d3d4b0e23a70bc65b5b972a6b65ffe456744691b1e5ee629efa`  
		Last Modified: Tue, 13 Jan 2026 19:16:09 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d659e8c3c8f5107f7ef2fa99a0ff03931440975b7b2496891b889249fd44a0bf`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab23b595a9fdc547ae2335b975d908db471bb1ca9fa7aae35ae5d170c77bf969`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baff20cf038ab062e6d0d73811bfb48cc11f10a5710d053ec8f14f49aa3b448`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7cf17a1c63aaa06502a03a33622b70549c07459ed7b8c3b04d8734b1c6c3a1`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.4` - unknown; unknown

```console
$ docker pull kibana@sha256:4057492ef88b0ddbc6ea82e62b3ec7b47501b141cbc56d7a98ae90a8eebed80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f64dc46fd0ac655ebf17dcf9b5bd44021e1b28f466a7c7023ff641f6a1e1f26`

```dockerfile
```

-	Layers:
	-	`sha256:e31fa34ed00a30baa744230e581ef08b01d97f6f0b729695657774e753610c2d`  
		Last Modified: Tue, 13 Jan 2026 21:11:45 GMT  
		Size: 5.8 MB (5750291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2843fa70f64fc60b6dbe28ad123e374166ab20444b78a60f83d9a4c46877b41b`  
		Last Modified: Tue, 13 Jan 2026 19:16:06 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:792f79b198075221dd70b8bc3ad31e32dff279fd882811f4af6ebc7ebf2ecd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.4 MB (459361329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed87099abba59416d6aa4391ecf49438e67a8462aa0ccdca1e09ff99f59f2646`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 13 Jan 2026 19:06:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:06:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:13:39 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:13:40 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:13:40 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:13:40 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:13:41 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:13:42 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:13:42 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:13:42 GMT
LABEL org.label-schema.build-date=2026-01-08T21:40:45.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b05a85503d4590280c7e9263175269a5f4a09729 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T21:40:45.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b05a85503d4590280c7e9263175269a5f4a09729 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 13 Jan 2026 19:13:42 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 13 Jan 2026 19:13:42 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:13:42 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:13:42 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:13:42 GMT
USER 1000
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dfe0b549339ca1d6d59332208080f200e2457e4b7f6d9dd0da4b481dbf361`  
		Last Modified: Tue, 13 Jan 2026 19:15:01 GMT  
		Size: 19.5 MB (19479548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8295c4a80b890d6044aa7979972b80ab7dbeb5b2a3b878e83ffbfc2d5bacefe6`  
		Last Modified: Tue, 13 Jan 2026 19:16:23 GMT  
		Size: 385.1 MB (385102079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2358211d34c8d307119843cc6d1a9b1e325d8230357308c5b438b6749c19357`  
		Last Modified: Tue, 13 Jan 2026 19:14:46 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f299218803ee977a72f4326dda1e0b81b2ea311f0dc7cef17741887f0c5a554`  
		Last Modified: Tue, 13 Jan 2026 19:15:10 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404f77b7a0e385f70f3528ffd525e5b6edb4993c35e0225793db07efbb95b585`  
		Last Modified: Tue, 13 Jan 2026 19:15:06 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf91a8c6051786a1b706ba20b41d963980f16bdddd5e952d75dcfee16f4a50d`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1bd4de5efdef4a3b69fbf5e376f43187e316cffbb1be32a83a99151afc8eed`  
		Last Modified: Tue, 13 Jan 2026 19:14:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568dc4c0c64804981aeb2a2f332de403da9dfa65f37fe894f2380801c65530f4`  
		Last Modified: Tue, 13 Jan 2026 19:14:48 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f1df4183608ec3c0f41fb66231a38ef2a99e3aab23edc34fcef118366eeeb7`  
		Last Modified: Tue, 13 Jan 2026 19:14:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9690d7cbb2e2dcc8da03363c9cc9e17028d712e83bf2304b7d60d5ce1c167e`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f2219d46c8f7e50444170a7d7b6b1d8b5e62815b4c7b44c81e9c499c73bfaf`  
		Last Modified: Tue, 13 Jan 2026 19:14:50 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d985d907b280bdbeafa80861bbcfbdf91d43e5ab08f4ecc1b1a33c411e590428`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.4` - unknown; unknown

```console
$ docker pull kibana@sha256:3fe6873a9f972c7b1cf92685f345cf6b62bccffc9859da32d7ac084015dd6478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecad4edf883d9c5e7e90b741c79553831c5108f7b6a35cb53e83237504bab9d0`

```dockerfile
```

-	Layers:
	-	`sha256:f3e4b713f2e8ce5a08ed48831268d2956b2ad2070ebe5ba598888e791ada22aa`  
		Last Modified: Tue, 13 Jan 2026 21:11:52 GMT  
		Size: 5.7 MB (5748963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f53931f09df7827f07ccff63266be390264ce7745eeb1ad1f2e17067f6e72c`  
		Last Modified: Tue, 13 Jan 2026 21:11:53 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
