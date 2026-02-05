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
$ docker pull kibana@sha256:da5a949e11b5b3486d73f7efc145b475ad58c666a6a569d2385fadcd8477ec92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.10` - linux; amd64

```console
$ docker pull kibana@sha256:9d12b5aaab0cd3838ee51c100b663ef19ae97dd0061627accf052a433c854c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441426721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb1743cca08c841baafcdb2b1b7da8957f3639870cd0f256d54168617c70916`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:15 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 19:50:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:58:56 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 19:58:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:58:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 19:58:56 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 19:58:56 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 19:58:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 19:58:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:58:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:58:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 19:58:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:58:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 19:58:58 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 19:58:58 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 19:58:58 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Thu, 05 Feb 2026 19:58:58 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 19:58:58 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:58:58 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 19:58:58 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 19:58:58 GMT
USER 1000
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26ab66f9060ce71ea9b0f4857e3107f256298af9e41eb9d3298060bfa4b929`  
		Last Modified: Thu, 05 Feb 2026 19:59:55 GMT  
		Size: 19.5 MB (19525195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e656c87eba9d80565b1e22b756d516942090c9446918b498bc6bfce76f49acfc`  
		Last Modified: Thu, 05 Feb 2026 20:00:01 GMT  
		Size: 365.3 MB (365287399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26719c1c4a2f18d6611a0cf676da82a2f2701ab1acd9e92e85a70935510a2a68`  
		Last Modified: Thu, 05 Feb 2026 19:59:54 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8210e6dc62875b3a84951d71741544bf155cdf3629c38ad7a099194f7f3e5f`  
		Last Modified: Thu, 05 Feb 2026 19:59:55 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279241d96bd02b57de68b48eb56ef6da020a7d72e73af9311ae4539bb5824e30`  
		Last Modified: Thu, 05 Feb 2026 19:59:55 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446b58b6b8924b0fc13f7ac4d23d95cc90f6e1c67a7feec2bdb62d62ad972553`  
		Last Modified: Thu, 05 Feb 2026 19:59:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5e71e352d863545304d7adf9cd213771edcff9dc3f5f6a8bd824a69d0c0b1f`  
		Last Modified: Thu, 05 Feb 2026 19:59:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa8539d0e41925621adf2a4d4b97eb6ef82d0c58e0ad3f2418e912b52e2698`  
		Last Modified: Thu, 05 Feb 2026 19:59:57 GMT  
		Size: 4.7 KB (4741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023955a6b93589cdc93e1194194f6b7c3a21f56ce37be210a0c68d9130d51417`  
		Last Modified: Thu, 05 Feb 2026 19:59:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab41482a2fa80e13d505adc4017b5b44d38055b718cb7719936473ebec97c35`  
		Last Modified: Thu, 05 Feb 2026 19:59:58 GMT  
		Size: 74.5 KB (74538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d993b52121dccc5b9fe040c84c3bec6b37cebcb845cc720387b9ee5d2e62b4`  
		Last Modified: Thu, 05 Feb 2026 19:59:58 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e53f569894f4778d8d6afc5b09d4fb28d7a71f797767a0903226f66760d26c`  
		Last Modified: Thu, 05 Feb 2026 19:59:59 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:73ba2eb5338767ff657b0e46c81f032afd2bc74df0ac18890b0c49fbaee93767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5718321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05af12c14be7109b65c504bda331915a2e49dd6a7c20445c238fb01e62c3ab1a`

```dockerfile
```

-	Layers:
	-	`sha256:7a7603d6b2ffe757d5cbfbd33817e488599a17141139a8a5b74883a8575254a2`  
		Last Modified: Thu, 05 Feb 2026 19:59:55 GMT  
		Size: 5.7 MB (5675088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4850707305c9b85acf40278c6b550ca4f65653004d04bbf1a53ff672aa2e67`  
		Last Modified: Thu, 05 Feb 2026 19:59:54 GMT  
		Size: 43.2 KB (43233 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:01431658ec1e6fa04028ce1576b2c6caf4ece513a071e514cfab037dba09620d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453236321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1cb1f08080b96169aa859ddb2c39a5a672334d6cffbc8bfa3da0b2f83928a0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:49:40 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 19:49:40 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:57:00 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 19:57:00 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:57:01 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 19:57:01 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 19:57:01 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 19:57:01 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 19:57:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:57:01 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:57:01 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 19:57:01 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:57:02 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 19:57:03 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 19:57:03 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 19:57:03 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Thu, 05 Feb 2026 19:57:03 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 19:57:03 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:57:03 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 19:57:03 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 19:57:03 GMT
USER 1000
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23262d482982caef37534bf6e663124f21e004bc4ca6c4b69f95950852636ac6`  
		Last Modified: Thu, 05 Feb 2026 19:58:07 GMT  
		Size: 19.5 MB (19477195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499473a44f690ceb5434446694bcbcdb6527af1a00a9fd0b5c1c3c14b5191b1f`  
		Last Modified: Thu, 05 Feb 2026 19:58:13 GMT  
		Size: 379.0 MB (378986610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecfb33e8431a53a1ee5348408a04fd2f11ab290c37289b3725c9898a4322161`  
		Last Modified: Thu, 05 Feb 2026 19:58:05 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09b61812239e0bbf89eab7bc8cb69c4ab240059e6f471d31d1a70397a56596`  
		Last Modified: Thu, 05 Feb 2026 19:58:06 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601257a7b5a28bc56d00b1713c580e541c2fde2c11fa25235df612eb2d904563`  
		Last Modified: Thu, 05 Feb 2026 19:58:06 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf99d5c54d3c737e0cb5fa4eb789b2e59119f7917a12e44707fb4d4a81718`  
		Last Modified: Thu, 05 Feb 2026 19:58:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915947d3de4a2e1f991a361aa1ca0efb8cb6e61e9476fa6a5f2e5b313a7c0e95`  
		Last Modified: Thu, 05 Feb 2026 19:58:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24924d116d49fac4bc792e245c9ccba139e52c3daa8849f1f81a2857d08f8239`  
		Last Modified: Thu, 05 Feb 2026 19:58:08 GMT  
		Size: 4.7 KB (4737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73aab1c49e52747ebb28fb0b7ee3978b9347da2f0955999444cf72fbd120cbc`  
		Last Modified: Thu, 05 Feb 2026 19:58:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7a1c8f21b7a518c0311a8f3053dd9c448b921d7fcf91d419520e5ee5641f80`  
		Last Modified: Thu, 05 Feb 2026 19:58:09 GMT  
		Size: 73.4 KB (73447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cc4b99d80e603428a055a6ba1660b36743ff820351d9e4b65d587fdbbffb98`  
		Last Modified: Thu, 05 Feb 2026 19:58:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864bb261a9e959e302bff910950ebcbce3c5ecd00f033b72bf5ba394ccb83581`  
		Last Modified: Thu, 05 Feb 2026 19:58:10 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:b1d7ff6eb5185f8bc49af9450b2eaa832ea78f5ed6ae8e37b1f5891d0930091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6330db8893cb51b27d9664b0068200b82d2fc82491162e558624e97c642bf29`

```dockerfile
```

-	Layers:
	-	`sha256:132fbe6b7d401d496f18210d5d23935dfa311a4988bca2b57c9e998f9a96b9a0`  
		Last Modified: Thu, 05 Feb 2026 19:58:06 GMT  
		Size: 5.7 MB (5673760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40e3d25f8f6d0bf4377cf215254b849251e0375743ec4ad76ebf2ac76cf6f27`  
		Last Modified: Thu, 05 Feb 2026 19:58:05 GMT  
		Size: 43.5 KB (43490 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.5`

```console
$ docker pull kibana@sha256:3d1da68c3992d5b83bc48e89f72b0375d9920333e3e1515a3badaedc26481f9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.5` - linux; amd64

```console
$ docker pull kibana@sha256:69b262ceda54999b228324f93dd44c28ebd06c7cf267f9bd14532ee3f0d23b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.2 MB (449184194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35410234b730148f58c28de70010bc7896d633e257490943e3c9cdea850abd3`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:15 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 19:50:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:59:00 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 19:59:00 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:59:00 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 19:59:00 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 19:59:01 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 19:59:01 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 19:59:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:59:01 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:59:01 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 19:59:01 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:59:01 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 19:59:02 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 19:59:02 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 19:59:02 GMT
LABEL org.label-schema.build-date=2026-01-28T23:38:44.165Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f99524135b3b29ff4011629c9e8511086b1a597a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T23:38:44.165Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f99524135b3b29ff4011629c9e8511086b1a597a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Thu, 05 Feb 2026 19:59:02 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 19:59:02 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:59:02 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 19:59:02 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 19:59:02 GMT
USER 1000
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60de2f1574f69fae11c641d0c485c33c228378d2f6772a521110f9bcaff3af9`  
		Last Modified: Thu, 05 Feb 2026 19:59:57 GMT  
		Size: 19.5 MB (19525187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292ea2ed34880d6a4be707c263b8b8ebf5dab3091660f682f9ce851b8bb7f35f`  
		Last Modified: Thu, 05 Feb 2026 20:00:04 GMT  
		Size: 373.0 MB (373044729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd30c6ba6eae0ec419a2384552c99242f55febe2b668e8e5d47b1b9769a539b9`  
		Last Modified: Thu, 05 Feb 2026 19:59:56 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6235015be8fd65a91e93a07b71461d7faabaa3173419428bfd41266f4aaa012e`  
		Last Modified: Thu, 05 Feb 2026 19:59:57 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22128d4f887d6642ada754fc8a8ef1d283f86183558c2ffac4841032999c498`  
		Last Modified: Thu, 05 Feb 2026 19:59:57 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed851b347f2becbf2f631530b4c9c9ea695e871404e725072e4e699f6174d69`  
		Last Modified: Thu, 05 Feb 2026 19:59:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2ff80d2e504e18ee6ae57fe60cc1816d09702202c49b788433ea4c405aeb0d`  
		Last Modified: Thu, 05 Feb 2026 19:59:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd74919a3ccfdd46805f129bd6be056e954e80cd64720b7006caa16404b7319`  
		Last Modified: Thu, 05 Feb 2026 19:59:58 GMT  
		Size: 4.9 KB (4894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6250ef3f5ba4a7080c98bce51ff08d69b1dcc66105fec119f792b166cec9e2b0`  
		Last Modified: Thu, 05 Feb 2026 20:00:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfd449a95582222c1dedc63eef602ddd7db06981de0abf117aaee18a4bda28a`  
		Last Modified: Thu, 05 Feb 2026 20:00:00 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69710d88a258030dc3b93ee9f6874021c97e15dde5fdb2cad77f01a6bfc4366`  
		Last Modified: Thu, 05 Feb 2026 20:00:00 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b56bd5977abcb8a4c9dd37233e907a4b0064f86988bed2e7fb8e99e897addb`  
		Last Modified: Thu, 05 Feb 2026 20:00:01 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.5` - unknown; unknown

```console
$ docker pull kibana@sha256:68f43b90f41173c2633264b567e192c49d7ee6ac9e56178b31afa3bbf8232c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5790835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2eedf42fe1098fd47f346eaa3438188a8babaf4713da655d7755a579bc568df`

```dockerfile
```

-	Layers:
	-	`sha256:98488834842d9aba27af96dc7be431ec0dfb3cfb1e96ffb018802931172073a7`  
		Last Modified: Thu, 05 Feb 2026 19:59:56 GMT  
		Size: 5.7 MB (5747609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2ff76a94961c28a04a6a4fc8e80e45f671e4552c00a9177a211e21f75aa912`  
		Last Modified: Thu, 05 Feb 2026 19:59:56 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e2cfc9b53ad70b962ad31cd8f116821c0cc24bfa67f81a7a11e932610fa32cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461021216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afac0b910d19275c2655f15c6f2142b64b3de9cda000f02865d33f41e0709da`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:49:54 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 19:49:54 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:57:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 19:57:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:57:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 19:57:27 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 19:57:27 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 19:57:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 19:57:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:57:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:57:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 19:57:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:57:28 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 19:57:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 19:57:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 19:57:29 GMT
LABEL org.label-schema.build-date=2026-01-28T23:38:44.165Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f99524135b3b29ff4011629c9e8511086b1a597a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T23:38:44.165Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f99524135b3b29ff4011629c9e8511086b1a597a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Thu, 05 Feb 2026 19:57:29 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 19:57:29 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:57:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 19:57:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 19:57:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28339ff02332a6f840fd948ecf68e2e59bc9a20189e24b13b80ccf1cd3d8f9b`  
		Last Modified: Thu, 05 Feb 2026 19:58:33 GMT  
		Size: 19.5 MB (19477205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaf870a3a07943f43b17356f195a9d8a06cf7324b43033cbf51f4bc4a5001cd`  
		Last Modified: Thu, 05 Feb 2026 19:58:40 GMT  
		Size: 386.8 MB (386771341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba330459c76ca31b96ce81844ec7de353c730926b976780a45b107e3185d2b9`  
		Last Modified: Thu, 05 Feb 2026 19:58:32 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434989a4a87486a0fcb3db3327088b519adf207d70d3af13d12b978773a9c627`  
		Last Modified: Thu, 05 Feb 2026 19:58:33 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6491d8804c4a40d1560c1a7a4e009de7fe95d3ac695b3c28402b2378a27620e2`  
		Last Modified: Thu, 05 Feb 2026 19:58:33 GMT  
		Size: 5.2 KB (5219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d81b2b7a49b0d7e87569d54fbd30d879ddaf18bbb1829648e21d8845faaad5`  
		Last Modified: Thu, 05 Feb 2026 19:58:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801631d2946b13940b8ed888516ace7a19afc1e6b31dde0617f8c86bf3927d2c`  
		Last Modified: Thu, 05 Feb 2026 19:58:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7c8fa4399ee5a61ba2e7670768fe1d547b5ae27cd661f7774dcf68a1e75d1f`  
		Last Modified: Thu, 05 Feb 2026 19:58:35 GMT  
		Size: 4.9 KB (4888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd00173943f40089c9058158dc58bf0a2595bf16d759fbbb1817fb8c8d9fa2`  
		Last Modified: Thu, 05 Feb 2026 19:58:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98405f9d7272f32cf83de06ec9cad5cee23544d75488e976d87150a5128be4b6`  
		Last Modified: Thu, 05 Feb 2026 19:58:36 GMT  
		Size: 73.4 KB (73445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a2885bc8ddee88dd2953e64bf3d5722f83954252213898e34a098f3dc23e0`  
		Last Modified: Thu, 05 Feb 2026 19:58:36 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd75d88e080a01a58ca6aa59e59138c923019cb00b517570e81bd5a6e576dd51`  
		Last Modified: Thu, 05 Feb 2026 19:58:37 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.5` - unknown; unknown

```console
$ docker pull kibana@sha256:fb2a3f07022943ee971e02c4eb23cf90720aa994ff98ec196316493e704bf678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded1d8935423b192dd054138869029904f49d0a1a2fd3d5738c5fe6acd437603`

```dockerfile
```

-	Layers:
	-	`sha256:0e0f41056bd805366b168291528647a396119dd8a6a1ccf3c6391f663d49db0c`  
		Last Modified: Thu, 05 Feb 2026 19:58:32 GMT  
		Size: 5.7 MB (5746281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1896e0b3455a126d6e6400c0b48c6ff5a7d98976118d4329add03949665e3c77`  
		Last Modified: Thu, 05 Feb 2026 19:58:32 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.0`

```console
$ docker pull kibana@sha256:f776c201f3d7d2bc021a1b986d9e4504028bd076957962be35503ef9fa6f5330
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.0` - linux; amd64

```console
$ docker pull kibana@sha256:b946c80983b415ad0bbec149d72be39635da4e29b7050d64fe2de39cae6285c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.9 MB (453881872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f440da4415dde490f4029432ccc3c87d41fbb5648eb0c3b05c222efc46c73bc7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:57:26 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:57:26 GMT
ENV container oci
# Thu, 05 Feb 2026 04:57:27 GMT
COPY dir:045ee84cbf9f515d46f16866a480828e69331a2895b4a0d38aab70097694b23c in /      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:57:27 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:57:27 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
COPY file:0fae80ad6e3e7d633c86e8adf8110f5657a4ca0224252ae63b130effe61540e7 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:57:28 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:57:10Z" "org.opencontainers.image.created"="2026-02-05T04:57:10Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:57:10Z
# Thu, 05 Feb 2026 19:50:16 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 19:50:16 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:59:36 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 19:59:37 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:59:37 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 19:59:37 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 19:59:37 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 19:59:37 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 19:59:37 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:59:37 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:59:37 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 19:59:37 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:59:38 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 19:59:39 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 19:59:39 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 19:59:39 GMT
LABEL org.label-schema.build-date=2026-01-29T09:38:21.004Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=30ab63cc0017fe2da7a84fb9b285dd762468802d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T09:38:21.004Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=30ab63cc0017fe2da7a84fb9b285dd762468802d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Thu, 05 Feb 2026 19:59:39 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 19:59:39 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:59:39 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 19:59:39 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 19:59:39 GMT
USER 1000
```

-	Layers:
	-	`sha256:f5b60ea3b234d3169587f4127ec6855e8be2c29e3f0ef963207f1ea8be32f8d1`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 40.1 MB (40055891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27bb35c83ce92dc529d7a2a4325d06d8dda32e8b5cdb4244bee846911c10330`  
		Last Modified: Thu, 05 Feb 2026 20:00:36 GMT  
		Size: 19.5 MB (19525198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb63f5d3192ca4ae1ba4b02ec57f206bcf05a0fa779b000c0fd00a6092691d47`  
		Last Modified: Thu, 05 Feb 2026 20:00:44 GMT  
		Size: 377.7 MB (377742390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a81e7cb5e4827f30e57e5bfbaa502b9079a811436288c469438d6dd3a7c914e`  
		Last Modified: Thu, 05 Feb 2026 20:00:37 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddb95a69d3650f9b93e4622b1b0e085e6314c526514f254099a80e41266a177`  
		Last Modified: Thu, 05 Feb 2026 20:00:36 GMT  
		Size: 16.5 MB (16460474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ebe2173c3f3502eb6dbd27549c22fe6e35a76e1d6d3a1f01ead2138271f70d`  
		Last Modified: Thu, 05 Feb 2026 20:00:38 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57af077a43c84ff7f46c92d53da51056f7a51828f59eb7384bee1910017c7d`  
		Last Modified: Thu, 05 Feb 2026 20:00:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb2b87a9033c40c4752f2a161f144ed02d6dbf2b4f955c6b1ea0062a84f354b`  
		Last Modified: Thu, 05 Feb 2026 20:00:38 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537a4b9c9bc741471142577147ca30cd6ab230386adc778b1c75432e528a55f0`  
		Last Modified: Thu, 05 Feb 2026 20:00:40 GMT  
		Size: 4.9 KB (4915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5a1e351811a800723417d26b656a82963e197cebdf3b787cac5caeb98ff480`  
		Last Modified: Thu, 05 Feb 2026 20:00:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fa59bc05f476653435130f17f4cf3858f3aee27610bace240e5b9f1558c246`  
		Last Modified: Thu, 05 Feb 2026 20:00:40 GMT  
		Size: 74.5 KB (74538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527b1b574c99bbb77bb1c8fbbbfaa7677a7201a2c632d571d68e9944a1ccd323`  
		Last Modified: Thu, 05 Feb 2026 20:00:42 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef9d09ec6b2aea7a87ee93966deff86929e2232ea4fa335fe8ab82558e21737`  
		Last Modified: Thu, 05 Feb 2026 20:00:43 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.0` - unknown; unknown

```console
$ docker pull kibana@sha256:679bb45239e4e3d5f063aaafae55ab4f9f2da2ad32f1a04ac3821f73e54ef3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccd55c2a6e1f826544b1ee6fecfcc3623e17032ed502c5e299c4bfb710e21c2`

```dockerfile
```

-	Layers:
	-	`sha256:ca113e60f7ebb8ecc554c95e379be561116675b1d4ca0271e1a388ed97431b17`  
		Last Modified: Thu, 05 Feb 2026 20:00:36 GMT  
		Size: 5.8 MB (5813728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:400f23fc68025ce50c0c16d6cb982ffe1a2e36d65a3bff5ebb5dae24be8fb96c`  
		Last Modified: Thu, 05 Feb 2026 20:00:36 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d62e08aa3a71907c86621544d97976610be2708f93441f96bddecab52dd9a2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.7 MB (465719148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3e4c74d1d13bd8e21adb983d63274ff6a3fb317ee961ac6e7bd3dcc5e161d0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 05 Feb 2026 04:59:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 05 Feb 2026 04:59:52 GMT
ENV container oci
# Thu, 05 Feb 2026 04:59:53 GMT
COPY dir:7899936d8a255ef23a03d65107dd50f0ce4a76df58676bb1ea68c1d8f5eabde0 in /      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 05 Feb 2026 04:59:53 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /usr/share/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:53 GMT
COPY file:b64f911bc23faf159ec29ad1e64fddab46c614bc74ee27e80c6fc4beab268d18 in /root/buildinfo/labels.json      
# Thu, 05 Feb 2026 04:59:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21849199b7179dc3074812b8e24698ec609d6a5c" "org.opencontainers.image.revision"="21849199b7179dc3074812b8e24698ec609d6a5c" "build-date"="2026-02-05T04:59:37Z" "org.opencontainers.image.created"="2026-02-05T04:59:37Z" "release"="1770267347"org.opencontainers.image.revision=21849199b7179dc3074812b8e24698ec609d6a5c,org.opencontainers.image.created=2026-02-05T04:59:37Z
# Thu, 05 Feb 2026 19:50:01 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 19:50:01 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 19:57:22 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 19:57:22 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 19:57:23 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 19:57:23 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 19:57:23 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 19:57:23 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 19:57:23 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 19:57:23 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 19:57:23 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 19:57:23 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 19:57:24 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 19:57:25 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 19:57:25 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 19:57:25 GMT
LABEL org.label-schema.build-date=2026-01-29T09:38:21.004Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=30ab63cc0017fe2da7a84fb9b285dd762468802d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T09:38:21.004Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=30ab63cc0017fe2da7a84fb9b285dd762468802d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Thu, 05 Feb 2026 19:57:25 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 19:57:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 19:57:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 19:57:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 19:57:25 GMT
USER 1000
```

-	Layers:
	-	`sha256:98b6d07e44e6381dc4b3ade3722986a976bbef5c5b424427e55892cfb27a03a0`  
		Last Modified: Thu, 05 Feb 2026 06:02:24 GMT  
		Size: 38.2 MB (38215820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88da965ede5e2ea6a6d019f9b3aa1dbe1a5c45c93b00af3b5e20981225163a5a`  
		Last Modified: Thu, 05 Feb 2026 19:58:31 GMT  
		Size: 19.5 MB (19477195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c9b6f7904c15912b6e934250dd24c9187d09e174f2652fb26d101ebf23e8e7`  
		Last Modified: Thu, 05 Feb 2026 19:58:43 GMT  
		Size: 391.5 MB (391469260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f02de750c85cbec13591c06891b0841759f2b875d8b5c4d7a2b31a549319b9`  
		Last Modified: Thu, 05 Feb 2026 19:58:29 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5361dd68056c85442fe9419385ec80dca96bde0201799185256557106e6fb14d`  
		Last Modified: Thu, 05 Feb 2026 19:58:31 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1b31039d2bd87913ef6b89687a757edc59456bf3510a784d0b8b4cfdf8992b`  
		Last Modified: Thu, 05 Feb 2026 19:58:31 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92fe3a9be2e77a0269713f24f2629a52257c91731381c1bf11d0a62f0abf5bf`  
		Last Modified: Thu, 05 Feb 2026 19:58:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c75d13ea299db2252c13f0edef4aad05f8fd302d0d9a15ac91e11d85778e6c7`  
		Last Modified: Thu, 05 Feb 2026 19:58:32 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f19fb848181e0ce0a943d6af677fddd3a951f9ca8b8aceba6db3c5d73e2fd`  
		Last Modified: Thu, 05 Feb 2026 19:58:33 GMT  
		Size: 4.9 KB (4910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41673faced6b308286b12baf6de9419cfc25dd9164639efd50b1a4f2054ba1bc`  
		Last Modified: Thu, 05 Feb 2026 19:58:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51932b68b93650d807c3f4027dfa8e7023eea6f6338267bbc1dd255a8fcd7c92`  
		Last Modified: Thu, 05 Feb 2026 19:58:33 GMT  
		Size: 73.4 KB (73447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a62db6a9bf7e26f3a3d7afdd4cd6abe53008f0f3d87f4d7142f0e4185c0e13`  
		Last Modified: Thu, 05 Feb 2026 19:58:34 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baab9d6f3c595ae09b95bf4975d6ebff0480b55b97da9239c7faa02b25c9f0c`  
		Last Modified: Thu, 05 Feb 2026 19:58:34 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.0` - unknown; unknown

```console
$ docker pull kibana@sha256:10fca45d7494aa2ea7f3487c593f88cb635b8602f0d0e5a5a70d999a5eb088e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288945dc52771c170f52bad54ba1f34fe8e64a7012095b93f7023bc8ba1fe4c7`

```dockerfile
```

-	Layers:
	-	`sha256:14c31718d1d408c263a54688e63dad828a4783e4e7e27e9d697501390837f57d`  
		Last Modified: Thu, 05 Feb 2026 19:58:30 GMT  
		Size: 5.8 MB (5812400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83edf0698fd5556d88c50ac10b0e7250d453fd2c8a4428af6b9988370b0c2aab`  
		Last Modified: Thu, 05 Feb 2026 19:58:29 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json
