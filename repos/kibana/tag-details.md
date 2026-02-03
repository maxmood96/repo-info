<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.11`](#kibana81911)
-	[`kibana:9.1.10`](#kibana9110)
-	[`kibana:9.2.5`](#kibana925)
-	[`kibana:9.3.0`](#kibana930)

## `kibana:8.19.11`

```console
$ docker pull kibana@sha256:9d578740a749a946306dabf7a07dd767333e49667d7ffe4433773d14aea43130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.11` - linux; amd64

```console
$ docker pull kibana@sha256:e25a464cf436c970bdd84eb60a8ab1a2c0783b7606376ffded60b8cc231d92bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.4 MB (444385194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f4c4988c25d8b59595faf73312ed613a06c404fac5e3a934b512dff07356c9`
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
# Tue, 03 Feb 2026 18:58:05 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 03 Feb 2026 18:58:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 19:07:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 03 Feb 2026 19:07:05 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 19:07:05 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 03 Feb 2026 19:07:05 GMT
RUN fc-cache -v # buildkit
# Tue, 03 Feb 2026 19:07:05 GMT
WORKDIR /usr/share/kibana
# Tue, 03 Feb 2026 19:07:05 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 03 Feb 2026 19:07:05 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:07:05 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:07:05 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 03 Feb 2026 19:07:05 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:07:06 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 03 Feb 2026 19:07:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 03 Feb 2026 19:07:07 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 03 Feb 2026 19:07:07 GMT
LABEL org.label-schema.build-date=2026-01-28T21:14:33.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c14722b56e3d34d5203bd311e91f9ec49227b044 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.11 org.opencontainers.image.created=2026-01-28T21:14:33.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c14722b56e3d34d5203bd311e91f9ec49227b044 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.11
# Tue, 03 Feb 2026 19:07:07 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 03 Feb 2026 19:07:07 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 03 Feb 2026 19:07:07 GMT
USER 1000
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ab7cfb04e56de8f686ce4a5038204f3c81bd9f1fd6115b950a1aa4a5deeb7`  
		Last Modified: Tue, 03 Feb 2026 19:08:04 GMT  
		Size: 11.8 MB (11833048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1397798772573e86dd2ed64edb54b67adba89109d19c842d42100fcd65dafadf`  
		Last Modified: Tue, 03 Feb 2026 19:08:11 GMT  
		Size: 386.2 MB (386182416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c37a7ee41cb424cca0471ff4e4b324683dd0b5ac01abfa3aa1a23c1ca85374`  
		Last Modified: Tue, 03 Feb 2026 19:08:03 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074ccc2e49080516e66224aeb27285a69a9667f75ac69888f2e8e6060321fe55`  
		Last Modified: Tue, 03 Feb 2026 19:08:04 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6cafca8a824a3c5713de304452df81227c772c6b6b1a0c4512575cc112444b`  
		Last Modified: Tue, 03 Feb 2026 19:08:04 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e26817b072758e866a6af8947b058ef5ef88cebbcea09d0cf345ed76e73de`  
		Last Modified: Tue, 03 Feb 2026 19:08:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e08800708465c12e000500ebed869cd37578ed44f90f3c18616993be92cd5e`  
		Last Modified: Tue, 03 Feb 2026 19:08:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede03a10270ce9ab2cc09451f032b6571f2fe9fae8169dd29ce0c15ae30ad955`  
		Last Modified: Tue, 03 Feb 2026 19:08:06 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eb57f0c1c0f39edb1efc816327e4d5f8dc5deaac19ef3745313641e1df7b29`  
		Last Modified: Tue, 03 Feb 2026 19:08:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7548fafdd83a64cbafbd0f00c3c4491b843de60a541a8387082a86b3fbdad5`  
		Last Modified: Tue, 03 Feb 2026 19:08:07 GMT  
		Size: 161.5 KB (161460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94953cf43a672bb5e46db1e14dd483f90aff83293edbcd64a24872349487b9b8`  
		Last Modified: Tue, 03 Feb 2026 19:08:07 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.11` - unknown; unknown

```console
$ docker pull kibana@sha256:08600f950a40770d783060b5867392b1728d82a0e31ad96164795ccec29498ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950e1ad9f4d88198bfaf0a85422d418dece8e6dec3b134ebc0904fccfdbb1a72`

```dockerfile
```

-	Layers:
	-	`sha256:448be44871cdcdeaf4a21c05235b8beeab4cbc49acee494f3b10443134ddd985`  
		Last Modified: Tue, 03 Feb 2026 19:08:03 GMT  
		Size: 4.9 MB (4921988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e79742f7feacaaeff6c9d9717d895fc8e969c3132658bbcb3c418e8e776a432`  
		Last Modified: Tue, 03 Feb 2026 19:08:03 GMT  
		Size: 40.9 KB (40926 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.11` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:dd73da2484dfb0191fb45b6c350883d39e8a83ec67dfbe27469a45bd0b8cc63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.1 MB (457080739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e4a8e20a1a3b842569de64f6ab6db8b875ac20c54a2ff081ee0fa1841cffb0`
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
# Tue, 03 Feb 2026 18:58:11 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 03 Feb 2026 18:58:11 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 19:05:44 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 03 Feb 2026 19:05:44 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 19:05:44 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 03 Feb 2026 19:05:44 GMT
RUN fc-cache -v # buildkit
# Tue, 03 Feb 2026 19:05:44 GMT
WORKDIR /usr/share/kibana
# Tue, 03 Feb 2026 19:05:45 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 03 Feb 2026 19:05:45 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:05:45 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:05:45 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 03 Feb 2026 19:05:45 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:05:45 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 03 Feb 2026 19:05:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 03 Feb 2026 19:05:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 03 Feb 2026 19:05:47 GMT
LABEL org.label-schema.build-date=2026-01-28T21:14:33.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c14722b56e3d34d5203bd311e91f9ec49227b044 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.11 org.opencontainers.image.created=2026-01-28T21:14:33.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c14722b56e3d34d5203bd311e91f9ec49227b044 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.11
# Tue, 03 Feb 2026 19:05:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 03 Feb 2026 19:05:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 03 Feb 2026 19:05:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2380b2cdf6bb38aa77a0f565f6130a845329aa9ae7f60ada5a1660801cbf2b`  
		Last Modified: Tue, 03 Feb 2026 19:06:52 GMT  
		Size: 11.7 MB (11664748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601fda1f9412b0c3d8e5831615bcaa69aaa69f2e786f879baa95d70cc22682cd`  
		Last Modified: Tue, 03 Feb 2026 19:06:59 GMT  
		Size: 399.9 MB (399912324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670a22f299987eba56ef38a60cec779cfdda8e17664f654b6db6c2f3e44c6e64`  
		Last Modified: Tue, 03 Feb 2026 19:06:51 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbc6385f7c6ac4040f8d4a2da2c32d513dfb0f9c649c02a31a96556b7d7cc96`  
		Last Modified: Tue, 03 Feb 2026 19:06:52 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7b4e7319cf4883d45bbdfe4a6a2e1fe3bf29830807c59996053aa0d49482d0`  
		Last Modified: Tue, 03 Feb 2026 19:06:53 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cade3b9851aca983dc4d9b02cbb5cc209bdf6d90d9c9d53bd5f5d23c0b8ec9`  
		Last Modified: Tue, 03 Feb 2026 19:06:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b03434672d8b74c70b57d531a0f6e1c0a073a260671d070ec1313c0088fea1`  
		Last Modified: Tue, 03 Feb 2026 19:06:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f72214ed275b81a4e36444528d6d804bb34378fd07f17c9c5431bf0d7674eba`  
		Last Modified: Tue, 03 Feb 2026 19:06:54 GMT  
		Size: 4.8 KB (4820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07276ece4862c7daabde2f7d62a856b3893c3520455e8ef82d6bba93ba5af8b`  
		Last Modified: Tue, 03 Feb 2026 19:06:55 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0966f56927c7d950514caf90a048323c65a7f6f413a4ecef30ecdea29407a15`  
		Last Modified: Tue, 03 Feb 2026 19:06:55 GMT  
		Size: 158.0 KB (157998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bb0d91a54cdada6dbe3a8db84fd1d6259b88ac7adcdb4b549daf05f72958e2`  
		Last Modified: Tue, 03 Feb 2026 19:06:55 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.11` - unknown; unknown

```console
$ docker pull kibana@sha256:f5aca7b0121a1d9c4449debbc99194d847581926cc9a4996901a0e8dc878a669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4964227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9d7d6cfde85563095940313f005f663f7f749eb77240e8e413dc636cc09012`

```dockerfile
```

-	Layers:
	-	`sha256:d5059b8c52cdfe4c22c0a8a73cc9aa56ec625bfa943cd7035e9c4349d9b56563`  
		Last Modified: Tue, 03 Feb 2026 19:06:52 GMT  
		Size: 4.9 MB (4923052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef1a9f3841029a8391243ad0a145ede6d35a999f13a7b2cad6371f2b298290a`  
		Last Modified: Tue, 03 Feb 2026 19:06:51 GMT  
		Size: 41.2 KB (41175 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.10`

```console
$ docker pull kibana@sha256:5d154b68dba2e0a0caa9829138b4f3580f352c99a609fd6c378c7aa113762ecf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.10` - linux; amd64

```console
$ docker pull kibana@sha256:25a11c764798c8fe1d6286a3b895e8c4cff8a800e331dbc28676a3db20dcc003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441382793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d777bb3313aab3f1668466b6c29094d6f0cd2ead1273429b48e3a94e75fc10d6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Mon, 26 Jan 2026 22:07:17 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 26 Jan 2026 22:07:17 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:16:33 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
RUN fc-cache -v # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
WORKDIR /usr/share/kibana
# Mon, 26 Jan 2026 22:16:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:16:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:16:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 26 Jan 2026 22:16:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:16:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 26 Jan 2026 22:16:36 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 26 Jan 2026 22:16:36 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 26 Jan 2026 22:16:36 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Mon, 26 Jan 2026 22:16:36 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 26 Jan 2026 22:16:36 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:16:36 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 26 Jan 2026 22:16:36 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 26 Jan 2026 22:16:36 GMT
USER 1000
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b608db8a68d2bfe6b7b5f9c30b17e9d0168753be536df5ef3ea832be2acdbea2`  
		Last Modified: Mon, 26 Jan 2026 22:17:38 GMT  
		Size: 19.5 MB (19532080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b925079a510f81aadbbd17793e03bbf6da238ee250cac700b11508d2b0cef7`  
		Last Modified: Mon, 26 Jan 2026 22:17:49 GMT  
		Size: 365.3 MB (365287442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36e530c9051134e2587a03040f7d9d68e31425bcb87f11805b3a89d91db9cf1`  
		Last Modified: Mon, 26 Jan 2026 22:17:37 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6c4a1df6f0e24c90479afeb9c33f27edd7606ce9e346f626de422e8e4d68cb`  
		Last Modified: Mon, 26 Jan 2026 22:17:38 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdcc30720783850a0c6434def66c0a021d16ff8a74b1a3fdb6376cfb89f3360`  
		Last Modified: Mon, 26 Jan 2026 22:17:38 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8060acd7f66c46b7a1fcf68356762b5cff5d546835e0517f827cb025390387ca`  
		Last Modified: Mon, 26 Jan 2026 22:17:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86536da71ae87ac1ec8a3525c919025f5fc4bf35b520817c871c4abccc260562`  
		Last Modified: Mon, 26 Jan 2026 22:17:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f7e0adbfa9e260025784b868a789825f1393de2a9a45807251f11531007b3c`  
		Last Modified: Mon, 26 Jan 2026 22:17:39 GMT  
		Size: 4.7 KB (4744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167728bb28b7a463184153fa6bf908aad73e24eeb9a810bf6e3921591cbde827`  
		Last Modified: Mon, 26 Jan 2026 22:17:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e1618ad18f360ca2b74400cc6efba48bc7c7f8448a78f1aca206d7c452994a`  
		Last Modified: Mon, 26 Jan 2026 22:17:40 GMT  
		Size: 74.5 KB (74543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9be7f3b49c1e60a4c797f12eb968e9ad95a4d238e02cdab9a4d3e168ee076ca`  
		Last Modified: Mon, 26 Jan 2026 22:17:40 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0e268f744c9268aedd495d704301c8479a9a4b8d1ba03153940d40e8695a63`  
		Last Modified: Mon, 26 Jan 2026 22:17:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:c4933d950adf4497400c2a112da063ef9007699f6ef146246a307a9c2bd29911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5718277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d84dc664f575fefe7b112081238fc1f29c8194fff9a76d744956b89931805d`

```dockerfile
```

-	Layers:
	-	`sha256:6d2f9fb7ac32f9f0208b41e50310742b1eded5407dd51d7354ed89f64838370a`  
		Last Modified: Mon, 26 Jan 2026 22:17:37 GMT  
		Size: 5.7 MB (5675044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cfcd67081d0db4aa9d0c888df1835b817ce25be2cd23be72851cd75f7c92459`  
		Last Modified: Mon, 26 Jan 2026 22:17:37 GMT  
		Size: 43.2 KB (43233 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:237459dfc13f2089fd174f9c687d62fd2c59f8549bd35751d6d82b4a40796722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453245361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d79caa423b83786af0867cc4b1f81014d66090c1016a96235747133030710b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Mon, 26 Jan 2026 22:05:50 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 26 Jan 2026 22:05:50 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:13:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 26 Jan 2026 22:13:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
RUN fc-cache -v # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
WORKDIR /usr/share/kibana
# Mon, 26 Jan 2026 22:13:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 26 Jan 2026 22:13:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:13:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 26 Jan 2026 22:13:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 26 Jan 2026 22:13:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 26 Jan 2026 22:13:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 26 Jan 2026 22:13:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 26 Jan 2026 22:13:14 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Mon, 26 Jan 2026 22:13:14 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 26 Jan 2026 22:13:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 26 Jan 2026 22:13:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 26 Jan 2026 22:13:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 26 Jan 2026 22:13:14 GMT
USER 1000
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eafe883ea21b27f7eeecae1cd89ef78d4c5864bccdd6f5c11ae20be7cf9da9`  
		Last Modified: Mon, 26 Jan 2026 22:14:17 GMT  
		Size: 19.5 MB (19478425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530a02de0b9b50986d3094c2e7e630bf6003fe416beaef1a5110b4ec7698937`  
		Last Modified: Mon, 26 Jan 2026 22:14:24 GMT  
		Size: 379.0 MB (378986588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9955483382ba70c26a1b651b8e8cb7981a29a69cbbbfc71cc7dbe401d768b0b`  
		Last Modified: Mon, 26 Jan 2026 22:14:16 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13679e9df58660b6e4b1671846a54fbe911346e5667ecddad34f5bd1fc34e236`  
		Last Modified: Mon, 26 Jan 2026 22:14:17 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b28b7f60c03f1fc9debf7bfc620dec2b63cafeb3989f24dc6dc07fa35293ce`  
		Last Modified: Mon, 26 Jan 2026 22:14:17 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1e0f8205e8e4d520cdc51fa70c3fa42ff064b61109796ce039574313f04d6d`  
		Last Modified: Mon, 26 Jan 2026 22:14:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c3efd728184072f97bf634dffaac4227807285f1387b23920078f4fd756c1e`  
		Last Modified: Mon, 26 Jan 2026 22:14:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e0d032c19ae2096a83468af119b4bffe065c3750bf61ccf4e6f166d3834238`  
		Last Modified: Mon, 26 Jan 2026 22:14:18 GMT  
		Size: 4.7 KB (4744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477b2c6f544d9245f0d20d55ed840be26dc492156ef9b170e754aef391b4f613`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad30dbea184fd531a034262e0db758197224d8089cae3194e0d9b6d6d04e4dd`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77e5d68122e972fd5f487bf45a77dffb00747769bcbf61c58bc6b98e75419b0`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f75916cde2ed0773f7231d0f03271cb03d2b8938e50f2b0a9ca05d3541d065`  
		Last Modified: Mon, 26 Jan 2026 22:14:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:74584c9f0ca0734aef6b04469f3db6f47a3c0b61d6dbadd592482891e363e337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f255a0b6b0e98cd5a3ef516437d7c6cd83acf21f9f0327cdcf42fc94ac0be62d`

```dockerfile
```

-	Layers:
	-	`sha256:2f46490b59f6c6a0e058791354e70c12449085eb918ff27af55b78192d442263`  
		Last Modified: Mon, 26 Jan 2026 22:14:16 GMT  
		Size: 5.7 MB (5673716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87b34ea18e3e7bf1a67ece86d8670d03ce7170e880cf08ce8553cb220cfc56e1`  
		Last Modified: Mon, 26 Jan 2026 22:14:16 GMT  
		Size: 43.5 KB (43490 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.5`

```console
$ docker pull kibana@sha256:308e24c474f73504420c3bdef42622e7e6e5cd9d32f94648a0bc2699f7298885
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.5` - linux; amd64

```console
$ docker pull kibana@sha256:24bc74f3c0142be6769cf255c8583885b6ee31e7e25b65adc6c9539b3e857a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449138313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c95eb27b5a231ca76206e26994a45f61f08de8a174dbc4383744d2d68c0d50`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Tue, 03 Feb 2026 18:58:05 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 03 Feb 2026 18:58:05 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 03 Feb 2026 19:07:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 03 Feb 2026 19:07:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 19:07:14 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 03 Feb 2026 19:07:14 GMT
RUN fc-cache -v # buildkit
# Tue, 03 Feb 2026 19:07:14 GMT
WORKDIR /usr/share/kibana
# Tue, 03 Feb 2026 19:07:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 03 Feb 2026 19:07:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:07:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:07:15 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 03 Feb 2026 19:07:15 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:07:15 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 03 Feb 2026 19:07:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 03 Feb 2026 19:07:16 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 03 Feb 2026 19:07:16 GMT
LABEL org.label-schema.build-date=2026-01-28T23:38:44.165Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f99524135b3b29ff4011629c9e8511086b1a597a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T23:38:44.165Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f99524135b3b29ff4011629c9e8511086b1a597a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Tue, 03 Feb 2026 19:07:16 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 03 Feb 2026 19:07:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 03 Feb 2026 19:07:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 03 Feb 2026 19:07:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 03 Feb 2026 19:07:16 GMT
USER 1000
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28eac935e859c48e85680e929b814e5ea977ec56d90a7b9fb4cc98f8c13a0e4`  
		Last Modified: Tue, 03 Feb 2026 19:08:17 GMT  
		Size: 19.5 MB (19530111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1a1a0bdbb8cb84a3d78d41fff9739deba0446006cb34c6dbe0ff39bc7c31a2`  
		Last Modified: Tue, 03 Feb 2026 19:08:24 GMT  
		Size: 373.0 MB (373044789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7622df6c859558aff14847d82a2f7dd67676295ad71fd7a301f624b83e845dad`  
		Last Modified: Tue, 03 Feb 2026 19:08:16 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc528e7107d495cc223ea18c6c9d0e3174f387fa6ab1cad1863afe0e31d1e0a`  
		Last Modified: Tue, 03 Feb 2026 19:08:17 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526927e11e302b9d78d236a7302c648631ce31b2590c0adcc6eb7e50a86c8ac4`  
		Last Modified: Tue, 03 Feb 2026 19:08:17 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7564c0adf585344c77b078fde4197d9051227347f3f96c6c48764bc365b48f9`  
		Last Modified: Tue, 03 Feb 2026 19:08:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6c9473592db8e60c588de3b0f1ce9a051582763b63cd3c6b50f7396628a751`  
		Last Modified: Tue, 03 Feb 2026 19:08:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002d8aef9303157b55b746fb4f540042d9b47503b0f6f09a6e0b96c4fe560fed`  
		Last Modified: Tue, 03 Feb 2026 19:08:19 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6add84da1476196ba2e189a829ccabc5987fb7e34a5877207165fe262b8d64`  
		Last Modified: Tue, 03 Feb 2026 19:08:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610bba0590ec86ca8d581dd3bee5fcc0c4295d98d0143bf9d4135e229a6684be`  
		Last Modified: Tue, 03 Feb 2026 19:08:20 GMT  
		Size: 74.5 KB (74544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904ff5547108d2da8214dedda93666cf1fe928a28de9b4b37bee796a3c70ca17`  
		Last Modified: Tue, 03 Feb 2026 19:08:20 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daceebe222cdf38a253d97db060da4a9a7180cde91e776ecb84fec033f7e4ae`  
		Last Modified: Tue, 03 Feb 2026 19:08:21 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.5` - unknown; unknown

```console
$ docker pull kibana@sha256:34af0f0cd8c2286222ce0b46af54307cd7a237e4991a5211fdbabeec51cc5e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5790791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9052ec1eb0f9d23c3cec9dd01c24d041b4ffc57f71e7f4e15586d43b89b9d4f5`

```dockerfile
```

-	Layers:
	-	`sha256:ef4a061457965e471cd576d910cec8f23eed0fadb083ed447d3d09e6b7b47f87`  
		Last Modified: Tue, 03 Feb 2026 19:08:16 GMT  
		Size: 5.7 MB (5747565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e512165cb70a6982307d9e20ebafab4d8d0f9c24cee71b692553246ca92dcfc`  
		Last Modified: Tue, 03 Feb 2026 19:08:16 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:0b15954100c916158f9480f3a6dfe29c166822430c90e809beccd9031e6ec02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461034223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb7c617dc83c1fbd9d46a66367b757980b74d444d3f60c9fa7cce33bf263429`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Tue, 03 Feb 2026 18:59:33 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 03 Feb 2026 18:59:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 03 Feb 2026 19:07:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 03 Feb 2026 19:07:10 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 19:07:10 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 03 Feb 2026 19:07:10 GMT
RUN fc-cache -v # buildkit
# Tue, 03 Feb 2026 19:07:10 GMT
WORKDIR /usr/share/kibana
# Tue, 03 Feb 2026 19:07:10 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 03 Feb 2026 19:07:10 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:07:10 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:07:10 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 03 Feb 2026 19:07:10 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:07:11 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 03 Feb 2026 19:07:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 03 Feb 2026 19:07:12 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 03 Feb 2026 19:07:12 GMT
LABEL org.label-schema.build-date=2026-01-28T23:38:44.165Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f99524135b3b29ff4011629c9e8511086b1a597a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T23:38:44.165Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f99524135b3b29ff4011629c9e8511086b1a597a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Tue, 03 Feb 2026 19:07:12 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 03 Feb 2026 19:07:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 03 Feb 2026 19:07:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 03 Feb 2026 19:07:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 03 Feb 2026 19:07:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbb8f08b5a14840afd78ad8acca53fd73f272528fb366f6272eae3f4d30def6`  
		Last Modified: Tue, 03 Feb 2026 19:08:17 GMT  
		Size: 19.5 MB (19482408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477f173a10b9d072f1d0011205edb9c6acc1b02fe2a532d409551c0f0bb38363`  
		Last Modified: Tue, 03 Feb 2026 19:08:24 GMT  
		Size: 386.8 MB (386771322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065baea9bb0b866d926cbf2da09445549b8a61547e0b2998996cdb68efbb34d9`  
		Last Modified: Tue, 03 Feb 2026 19:08:15 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cfa0d0fa5bd62ffc45f34ad6c8874d1a639f02cafd551e02e68730b0728466`  
		Last Modified: Tue, 03 Feb 2026 19:08:17 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358221113f81e42778d1c7a51e5fa5adb82c9db1f6759533c97493553c0f4628`  
		Last Modified: Tue, 03 Feb 2026 19:08:17 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcdd47159f1ee9626cb8208eca13f79e4595ded9ce6476513735c3214fb90f3`  
		Last Modified: Tue, 03 Feb 2026 19:08:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c31ad3c394df7973945b4b0c2267a3cf24dde7be8136503be1642dfebf491e7`  
		Last Modified: Tue, 03 Feb 2026 19:08:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0275ca75ed53e080bf6bcef0ec503e11bb17b545468b6ea49e1ae10b4afa695`  
		Last Modified: Tue, 03 Feb 2026 19:08:18 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef4558fabea0724e12dbc36405101898aecdd51b9c3bcecb62621d65cdd9a33`  
		Last Modified: Tue, 03 Feb 2026 19:08:19 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc444dffbe2f765624971278d6a72d9b77f52a8cf58510102dc35a4fb3bebf31`  
		Last Modified: Tue, 03 Feb 2026 19:08:20 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d183f2acb2ae2636b1ef82627b9564c910ea265701a2942a9e87e3356c7150a`  
		Last Modified: Tue, 03 Feb 2026 19:08:20 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61287ea1ee5faed7b889696b83c0a86eacaba62bbb85f9ee074b24a28a4f4285`  
		Last Modified: Tue, 03 Feb 2026 19:08:20 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.5` - unknown; unknown

```console
$ docker pull kibana@sha256:133aa53d6bcaf69c9cb0d615e3288589f0856dc492b8f6cd64483d542728a307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec99bfbf847f1cb1d265610ce7da1b1a729ac9bd6edfde36885cd6b846be8b34`

```dockerfile
```

-	Layers:
	-	`sha256:9fe771e8f9a43c5e11e7c13d416aee34d8e95e387a0e1543a543518a090e65c6`  
		Last Modified: Tue, 03 Feb 2026 19:08:16 GMT  
		Size: 5.7 MB (5746237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8745387477dd74c2d3903f0e6b722ecdf68f6c7df3302a537e9b41e2522a94f`  
		Last Modified: Tue, 03 Feb 2026 19:08:15 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.0`

```console
$ docker pull kibana@sha256:921af7f9ba5ef00c0f76fa5f4e2cc5f26cf47c0fd3551efada9719a559e40875
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.0` - linux; amd64

```console
$ docker pull kibana@sha256:196f295260c43638c595d99f1f7f53aa75a49cf373482b9bfa01fc63b7529e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.8 MB (453835975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae4d685374321a28c1fd7db3ac709554219f35d278151b08fcd0f46547ffc52`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 22 Jan 2026 05:12:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:50 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 05:12:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 05:12:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 05:12:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 05:12:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 05:12:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 05:13:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 05:13:01 GMT
ENV container oci
# Thu, 22 Jan 2026 05:13:09 GMT
COPY dir:de0fcf5c4847724050e2f935a6ca475ba4c6d0b18e49a32c8b2e370255fb563e in /      
# Thu, 22 Jan 2026 05:13:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 05:13:13 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 05:13:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 05:13:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 05:13:19 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:21 GMT
COPY file:fb2ace2f51fa7133c2c5a93fa3c8bbf925b388bca60f9c67837af1935a7cbe40 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 05:13:37 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T05:09:47Z" "org.opencontainers.image.created"="2026-01-22T05:09:47Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T05:09:47Z
# Tue, 03 Feb 2026 18:58:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 03 Feb 2026 18:58:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 03 Feb 2026 19:07:59 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 03 Feb 2026 19:08:00 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 19:08:00 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 03 Feb 2026 19:08:00 GMT
RUN fc-cache -v # buildkit
# Tue, 03 Feb 2026 19:08:00 GMT
WORKDIR /usr/share/kibana
# Tue, 03 Feb 2026 19:08:00 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 03 Feb 2026 19:08:00 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:08:00 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:08:00 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 03 Feb 2026 19:08:00 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:08:01 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 03 Feb 2026 19:08:02 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 03 Feb 2026 19:08:02 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 03 Feb 2026 19:08:02 GMT
LABEL org.label-schema.build-date=2026-01-29T09:38:21.004Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=30ab63cc0017fe2da7a84fb9b285dd762468802d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T09:38:21.004Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=30ab63cc0017fe2da7a84fb9b285dd762468802d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Tue, 03 Feb 2026 19:08:02 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 03 Feb 2026 19:08:02 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 03 Feb 2026 19:08:02 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 03 Feb 2026 19:08:02 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 03 Feb 2026 19:08:02 GMT
USER 1000
```

-	Layers:
	-	`sha256:55c0205b422beeca9ab8ece9c61b1e34f31686b8a7adf249272ac75b4dd57e4d`  
		Last Modified: Mon, 26 Jan 2026 04:14:55 GMT  
		Size: 40.0 MB (40005014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3338933ceb5b38d7a5c8780bdec07fd52307e35b62d002e67d4e6c6854b60df1`  
		Last Modified: Tue, 03 Feb 2026 19:09:04 GMT  
		Size: 19.5 MB (19530145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1352ef11746647792241f82cc9766c52bb0deee08ac79eb6c08c7d14fd7be20f`  
		Last Modified: Tue, 03 Feb 2026 19:09:11 GMT  
		Size: 377.7 MB (377742395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89033a6437694323b0c7c3b28f730d8bbba09d9a6b430e3018fbc8d9b125cb`  
		Last Modified: Tue, 03 Feb 2026 19:09:02 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55017e5881c11eaa448a3ef2d13c2dd527ad478612f284866c7582d89739f70`  
		Last Modified: Tue, 03 Feb 2026 19:09:04 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365d7960972c2023bc6113b15ada79b587dd91bb77765296f6a0da70af657f18`  
		Last Modified: Tue, 03 Feb 2026 19:09:04 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36e7a785245eb10d10f5854e984a37105a4f1dcadb104e3acdfd39a7091aa28`  
		Last Modified: Tue, 03 Feb 2026 19:09:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a206a3526ac171d22e3e06e84748d74ba4e38938d2bf578e07e1e3ee7d1d2`  
		Last Modified: Tue, 03 Feb 2026 19:09:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f4d3244446c0b464bb0757c81c3c9f1303c2385c7988710e885febe2baf9a7`  
		Last Modified: Tue, 03 Feb 2026 19:09:05 GMT  
		Size: 4.9 KB (4921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771bbcc0c02136f0921de85bd4bc77177d3c49fe7b2156b6a8382d1b40a652b9`  
		Last Modified: Tue, 03 Feb 2026 19:09:06 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad55ec4ec40829072a7658f9167a7afcf32238bb3dfc01f491d632b9f9340216`  
		Last Modified: Tue, 03 Feb 2026 19:09:06 GMT  
		Size: 74.5 KB (74544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea701ad8ee3c421be6db6f2edc7098a856177932ed94bb4a57f2e321f00a0f8e`  
		Last Modified: Tue, 03 Feb 2026 19:09:07 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64480a229d6d260a55e6e42bdaea946683b6cc3b35ecc86b01b27d0920cf40de`  
		Last Modified: Tue, 03 Feb 2026 19:09:07 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.0` - unknown; unknown

```console
$ docker pull kibana@sha256:380807c9fa04cc31bd67e99597622039e0097f2c4076894cd12920c387018097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56d64a264e4bd7d5b2a03804356b6f4552b5bb90737ba364a2b7ba3429d5e91`

```dockerfile
```

-	Layers:
	-	`sha256:252d79b4272a04cf5bec228e38ed97e3ff244fed35f950682bf763fe7177be01`  
		Last Modified: Tue, 03 Feb 2026 19:09:03 GMT  
		Size: 5.8 MB (5813684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b40eca89fef2e48b0c26178228f59a1a9bb9a30787cbb9f5420017b5b64621a6`  
		Last Modified: Tue, 03 Feb 2026 19:09:02 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4ce98c8a4a33845428d6547021729c9951cac4f1ed282d2ffce5602aa269a5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.7 MB (465732528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2384ee345fc57764a3f560b28bbb0c8e92295b1e29c671beafb98632bace4bcb`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 04:46:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Jan 2026 04:47:00 GMT
ENV container oci
# Thu, 22 Jan 2026 04:47:00 GMT
COPY dir:5911db9f5450531429169fb3bc4d156204437f84bcda3e7b49af077219ecb148 in /      
# Thu, 22 Jan 2026 04:47:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 04:47:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
COPY file:57f009d4f4cb77bc277e064b341ab6fdc0d69d350d43f8a21909f2baad049960 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 04:47:01 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="812a20485e9d8d728e95b468c2886da21352b9fc" "org.opencontainers.image.revision"="812a20485e9d8d728e95b468c2886da21352b9fc" "build-date"="2026-01-22T04:46:44Z" "org.opencontainers.image.created"="2026-01-22T04:46:44Z" "release"="1769056855"org.opencontainers.image.revision=812a20485e9d8d728e95b468c2886da21352b9fc,org.opencontainers.image.created=2026-01-22T04:46:44Z
# Tue, 03 Feb 2026 19:01:41 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 03 Feb 2026 19:01:41 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 03 Feb 2026 19:09:31 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 03 Feb 2026 19:09:32 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Feb 2026 19:09:32 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 03 Feb 2026 19:09:32 GMT
RUN fc-cache -v # buildkit
# Tue, 03 Feb 2026 19:09:32 GMT
WORKDIR /usr/share/kibana
# Tue, 03 Feb 2026 19:09:32 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 03 Feb 2026 19:09:32 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Feb 2026 19:09:32 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 19:09:32 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 03 Feb 2026 19:09:32 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 19:09:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 03 Feb 2026 19:09:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 03 Feb 2026 19:09:34 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 03 Feb 2026 19:09:34 GMT
LABEL org.label-schema.build-date=2026-01-29T09:38:21.004Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=30ab63cc0017fe2da7a84fb9b285dd762468802d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T09:38:21.004Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=30ab63cc0017fe2da7a84fb9b285dd762468802d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Tue, 03 Feb 2026 19:09:34 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 03 Feb 2026 19:09:34 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 03 Feb 2026 19:09:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 03 Feb 2026 19:09:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 03 Feb 2026 19:09:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:acd46633fecc5c7b908a52adf94f664d167c28dd5a89ed681fe958b1c58c6963`  
		Last Modified: Mon, 26 Jan 2026 05:26:49 GMT  
		Size: 38.2 MB (38223626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76cf8b30c7f79c53219063220aa6ad86122df32781953104b84e9fb639a468d`  
		Last Modified: Tue, 03 Feb 2026 19:10:40 GMT  
		Size: 19.5 MB (19482726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4c18e8d5f89d5dadb4c7718700363596987df2761524ab63d359f226455679`  
		Last Modified: Tue, 03 Feb 2026 19:10:47 GMT  
		Size: 391.5 MB (391469281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74208fa0855b29e17819e8da3336ff1fef33a0b3a497e79773302d783c568580`  
		Last Modified: Tue, 03 Feb 2026 19:10:39 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376f55e6d6576af189941f6fb243a44aeb6100844064e91c32b6174c057aac8b`  
		Last Modified: Tue, 03 Feb 2026 19:10:40 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e704295e7f4cadbea1c30d661e7824c9b562cf948ec797ff6b8b5ad8a22b04a`  
		Last Modified: Tue, 03 Feb 2026 19:10:40 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0407c0c6544e6c4e1f0ab8a5db3ffb2386575b5dbac286fabbb6728579d9e7ae`  
		Last Modified: Tue, 03 Feb 2026 19:10:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2679fdcd3033001374ee8172c89ec9f11bed46d0eef7dd0ae2d17ebaf57fc5c`  
		Last Modified: Tue, 03 Feb 2026 19:10:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae647d9b875cd86d8eb0519427155323e8ddd300a09e732da32b1e2ada46eba0`  
		Last Modified: Tue, 03 Feb 2026 19:10:42 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede9f353955b6bef6ad3f043f571b91096cc04ceabed9d5863aac4632a1a7194`  
		Last Modified: Tue, 03 Feb 2026 19:10:43 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000c808eb7c129d302b2007631dcf82d140ecc8be3e694ada7d872eb79e64c5f`  
		Last Modified: Tue, 03 Feb 2026 19:10:43 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca60a3773e2af8f30612556277924745902b28255ae7bfc817c22aece3bed3a`  
		Last Modified: Tue, 03 Feb 2026 19:10:43 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de0d3ab990d2a96adc466d24be83f6d519f5a6c01c1d59134a2158e673bed79`  
		Last Modified: Tue, 03 Feb 2026 19:10:44 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.0` - unknown; unknown

```console
$ docker pull kibana@sha256:17304d0f8611be8d265d2282c3953e5ff1b6867b506a3c63515d1e4956d2782d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff136a14f4907df20902684783120d8fec1307a95c8c294881fc80159800fa80`

```dockerfile
```

-	Layers:
	-	`sha256:698aa163ab6555181509cc1161619d5ea8047976b5adc512e7aa8092e67aeedd`  
		Last Modified: Tue, 03 Feb 2026 19:10:39 GMT  
		Size: 5.8 MB (5812356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcc3d58715cc285af1b5f053bec34f85d007130d53678bef03aca872817576fe`  
		Last Modified: Tue, 03 Feb 2026 19:10:39 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
