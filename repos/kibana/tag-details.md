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
$ docker pull kibana@sha256:de285d22e7c92b948e34e2d22b55ecf55f7f6a10b7f5b2132e2b1c8d63beb5ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.10` - linux; amd64

```console
$ docker pull kibana@sha256:e24e6816a4a9c41508f2a0db8ab59a842eb0f6fd7b36341f267a5c7eb0fec361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441386013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b2dd21f2157fdd8035b0f02c10b7dee9b9d5cea73b57339629b259314ff996`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:08:57 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 00:08:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:17:55 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 00:17:55 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:17:55 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 00:17:56 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 00:17:56 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 00:17:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 00:17:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:17:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:17:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 00:17:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:17:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 00:17:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 00:17:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 00:17:57 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Thu, 05 Feb 2026 00:17:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 00:17:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:17:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 00:17:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 00:17:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87ee1260a3bf0ed2529b334bd4240576781779bfd6048502894fdfa0c829df4`  
		Last Modified: Thu, 05 Feb 2026 00:18:53 GMT  
		Size: 19.5 MB (19531281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd65662d42f468a60bfe90042f027da2bf5d5c4c83ccf8b54f5176aead04ba9`  
		Last Modified: Thu, 05 Feb 2026 00:19:00 GMT  
		Size: 365.3 MB (365287440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b03281e2737bd0aa2dfb59eb1f931b011a2b2beca107fa87abdb153d9a4a472`  
		Last Modified: Thu, 05 Feb 2026 00:18:51 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d0596633dc4a4fe973d266a5758e39d8b626aebf2b4efef2c862119332c4d2`  
		Last Modified: Thu, 05 Feb 2026 00:18:53 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef71783e80b9b523e18db860017cbfe37df46eddac88d80f47541c1393517b6`  
		Last Modified: Thu, 05 Feb 2026 00:18:53 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc3a5aacbd064a112d6410c877a0417cd57123cbc1404a532238eb7560018c7`  
		Last Modified: Thu, 05 Feb 2026 00:18:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bf714db83a6f6a3d91a61c9e324fef5df201efbb5bbc41128ab9fe7ae7724f`  
		Last Modified: Thu, 05 Feb 2026 00:18:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225419c0645ad9b2af614c79711f740d7bcca3cdcdcee6e9dbbaf0913ccc7733`  
		Last Modified: Thu, 05 Feb 2026 00:18:54 GMT  
		Size: 4.7 KB (4737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf356017e07969c6414f7d6d876563f3130bcca6674523cbdd1d857abaa593e2`  
		Last Modified: Thu, 05 Feb 2026 00:18:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4e2760971940bc3a37a3a0056a6a9f6fd6374ce51603922308fe38a76880de`  
		Last Modified: Thu, 05 Feb 2026 00:18:55 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c91e7e1fce2b99b6c97d526fc523f0239054aa619c607a0abfee66b344f769`  
		Last Modified: Thu, 05 Feb 2026 00:18:56 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e79198bc5bdb88be8e2b50e40628a35743815f8fcd525d1776ee8a95173c35a`  
		Last Modified: Thu, 05 Feb 2026 00:18:56 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:08e1ef10d931cf3bc1a25c053b3427ae4506c0f7ac68b45e3d5f5645d90719ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5718301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6d78021538276bc3b39952d26dd6c58642256cd1b77a09d52d5949ee925b94`

```dockerfile
```

-	Layers:
	-	`sha256:4b79860ee251ed958026d1edf242f892f58008ef5bd20b2fb2728480bb73c91d`  
		Last Modified: Thu, 05 Feb 2026 00:18:52 GMT  
		Size: 5.7 MB (5675068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7afa8bb4c57ae63a9a5638e856f924f3339a8d7f6163e4310d52078394ff2103`  
		Last Modified: Thu, 05 Feb 2026 00:18:51 GMT  
		Size: 43.2 KB (43233 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:92d4002d6832ff05e06c026b6a05111db9a61db92002bde24efbf031d5e2f119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453220645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1e4ddd2d6a1d2f50ccf8b64f80df768378fed6453406f7069169c808fa84b9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:08:29 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 00:08:29 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:15:52 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 00:15:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:15:53 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 00:15:53 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 00:15:53 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 00:15:53 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 00:15:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:15:53 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:15:53 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 00:15:53 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:15:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 00:15:55 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 00:15:55 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 00:15:55 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Thu, 05 Feb 2026 00:15:55 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 00:15:55 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:15:55 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 00:15:55 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 00:15:55 GMT
USER 1000
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aa31d134ab03d7213fd228f9098ec14b11a7624c059f67fa7cfc7db5013acd`  
		Last Modified: Thu, 05 Feb 2026 00:16:59 GMT  
		Size: 19.5 MB (19481614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad64cfba7449f310124b02ccd9004fe99a209efee81a2284bac34a3827a94f4`  
		Last Modified: Thu, 05 Feb 2026 00:17:09 GMT  
		Size: 379.0 MB (378986588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e9f58ee26dfe748a56c54e2e49f315541cae4c08d042b4d02f566a5d2f39b1`  
		Last Modified: Thu, 05 Feb 2026 00:16:57 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769d4d3c46488cb8d739cf4db3e1513307dfcaa2fb91fbe19872e55717e1d41`  
		Last Modified: Thu, 05 Feb 2026 00:16:59 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5d0de6a921f700b75c7dc611c3c3f1c19c8e9269fc2e5cb943e4c8563dea2f`  
		Last Modified: Thu, 05 Feb 2026 00:16:59 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c085a4c7da52d6c1d2409805d22506c547b778b473f5f666f48c304fcc47ec5`  
		Last Modified: Thu, 05 Feb 2026 00:17:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f31a1962ca5ab4ebe7fa36d0c50f58c97c9d50ea04534be7316b81f6ab2d51f`  
		Last Modified: Thu, 05 Feb 2026 00:17:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8fb97d1fe2703cbb3fb4755be4656e50e5d64a3979c63585a4af7111faa3c7`  
		Last Modified: Thu, 05 Feb 2026 00:17:01 GMT  
		Size: 4.7 KB (4743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de38036900cf95e58458cf29de8785af0500daec29b5edf007d5b1cd413c847`  
		Last Modified: Thu, 05 Feb 2026 00:17:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393781de3d19d192869e015e76d6e43f1914fcf8f8c37470e469062d684f4586`  
		Last Modified: Thu, 05 Feb 2026 00:17:02 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3346e44d30ae94b4066f57b1db0b3db7ff261decf541fdba3db9a71906a48aa5`  
		Last Modified: Thu, 05 Feb 2026 00:17:02 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1817004d97a92c8323c4bb068abadbe29f0f77e33f5f2290060a994355a9da6a`  
		Last Modified: Thu, 05 Feb 2026 00:17:03 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:8679fa4471d9650188ca6468d110da00a447807aaef6b516398a399e333e8927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b2ac9a9e65be79d4f25d07feb7939d8fc730a61f00b2f579291517fdc2609b`

```dockerfile
```

-	Layers:
	-	`sha256:361f273d8d9c04b3fb565fb3b8b9d36bffe60e07a73427e8a5823480dcc5a97f`  
		Last Modified: Thu, 05 Feb 2026 00:16:58 GMT  
		Size: 5.7 MB (5673740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2544be99313efec25f341af2850884ea0ccea7d6419d877033be7de1a7e57d9d`  
		Last Modified: Thu, 05 Feb 2026 00:16:57 GMT  
		Size: 43.5 KB (43490 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.5`

```console
$ docker pull kibana@sha256:1d0ff2a60666f412cff126d87c46117070d89d85a474bee96724d90dd2d05f8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.5` - linux; amd64

```console
$ docker pull kibana@sha256:c26cdad18ac0c3b1f6762b5c6a4c20f8755a391436f4248ec6e9f8e7560e7115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449143216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de984faf54bb302280d71c44ea0859d2c389e8f072548a47f02a0d0d4cd0173`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:09:01 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 00:09:01 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:18:17 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 00:18:17 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:18:17 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 00:18:18 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 00:18:18 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 00:18:18 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 00:18:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:18:18 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:18:18 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 00:18:18 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:18:18 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 00:18:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 00:18:19 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 00:18:19 GMT
LABEL org.label-schema.build-date=2026-01-28T23:38:44.165Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f99524135b3b29ff4011629c9e8511086b1a597a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T23:38:44.165Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f99524135b3b29ff4011629c9e8511086b1a597a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Thu, 05 Feb 2026 00:18:19 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 00:18:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:18:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 00:18:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 00:18:20 GMT
USER 1000
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b001dc568a3d87799a7e99fe2ac3d63446a23830d958a74166b7dc5b7d126f`  
		Last Modified: Thu, 05 Feb 2026 00:19:19 GMT  
		Size: 19.5 MB (19531021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07a75f9022ac43918614c01e343d05c138a65bf541b05e0c4754bff79ca2f94`  
		Last Modified: Thu, 05 Feb 2026 00:19:26 GMT  
		Size: 373.0 MB (373044737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69579d1a334b9b12d6020929fcdbaa928afd4f14b1a22095489ca549859e21ae`  
		Last Modified: Thu, 05 Feb 2026 00:19:18 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0236e6b1cb714d9b00f56ce42ab9b1ddb9fae38cd50558c6685cd019c248b5`  
		Last Modified: Thu, 05 Feb 2026 00:19:19 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb2040f9f31fa446611b6983404edf291ccffd673bbfdc62c4e1a2f6d8fdc04`  
		Last Modified: Thu, 05 Feb 2026 00:19:19 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e653766936ef4104ede7bdc0982476281ea40be9fbb89ce4c60769eabf953a`  
		Last Modified: Thu, 05 Feb 2026 00:19:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3f1b051ffa8897642c80aa225153e28f03b28fcf1b52424821e5104ac716cf`  
		Last Modified: Thu, 05 Feb 2026 00:19:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6faf904f2c8e85dd0fdbaa91b2ebe0b122a27f0d7cce24f678d5423d8a9ec9a`  
		Last Modified: Thu, 05 Feb 2026 00:19:21 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1989722527b06532770634e3a3c69a8dcdffb9caed1fd2831d9599c7bc542bad`  
		Last Modified: Thu, 05 Feb 2026 00:19:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b9cb4f4ba769d4a82fd39bb67f7a1dc5ed14824dca70bbf8c716e76415bac`  
		Last Modified: Thu, 05 Feb 2026 00:19:22 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1844ea47ad371b4e055937d64f304e845565aebc8469d7ca77ed3651faf88f9c`  
		Last Modified: Thu, 05 Feb 2026 00:19:22 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2b921fb3fe9602015ef0cda0742baad4f6e28e3c75ff4747a88abf74f3a065`  
		Last Modified: Thu, 05 Feb 2026 00:19:23 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.5` - unknown; unknown

```console
$ docker pull kibana@sha256:491a37bd2c31824b057ab521150478543b6ffc68c82690807732ea88fb1e523d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5790813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1599bcefa776926e3c1b76c8bdaa420daccd54725f37ae8c5894dff009c3d99a`

```dockerfile
```

-	Layers:
	-	`sha256:a5c8d8ff9fc9b089f1c7028fd04e2920669f0625203b34fc4b6a5ed0f573eaf4`  
		Last Modified: Thu, 05 Feb 2026 00:19:18 GMT  
		Size: 5.7 MB (5747589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd227ad8282f3fd8890594a1d4783379064428f9653a587ef2d0d12665cf3df`  
		Last Modified: Thu, 05 Feb 2026 00:19:18 GMT  
		Size: 43.2 KB (43224 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2c6c49a64d53f38ed6672f7a13b1c2fc6be524400c1e2b01d0e2237c799c15d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461005468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32d080c4a675593def649ec3599036d636400ee2d038bb177d18abd29fb1ea7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:08:38 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 00:08:38 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:16:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 00:16:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:16:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 00:16:12 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 00:16:12 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 00:16:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 00:16:12 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:16:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:16:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 00:16:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:16:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 00:16:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 00:16:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 00:16:14 GMT
LABEL org.label-schema.build-date=2026-01-28T23:38:44.165Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f99524135b3b29ff4011629c9e8511086b1a597a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T23:38:44.165Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f99524135b3b29ff4011629c9e8511086b1a597a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Thu, 05 Feb 2026 00:16:14 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 00:16:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:16:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 00:16:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 00:16:14 GMT
USER 1000
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdbe19d49519e806d9f5ba5656f9d18387dbda96cd1cd1c02574feee94eaaa9`  
		Last Modified: Thu, 05 Feb 2026 00:17:19 GMT  
		Size: 19.5 MB (19481595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747e6e8eb2c1cccd8effdc9ff7097615cc6e6e1d7d7950ed27f2c820f6909f28`  
		Last Modified: Thu, 05 Feb 2026 00:17:27 GMT  
		Size: 386.8 MB (386771287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ec664af15fcb24484bb128ecd01607ebe0315b6da7a0c2ba71eb109e37658`  
		Last Modified: Thu, 05 Feb 2026 00:17:18 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e22ff922a293d2a4a747fd39798ab6608c4b9cbd86cc730c48a8ad4de68b8b`  
		Last Modified: Thu, 05 Feb 2026 00:17:19 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b94fc5bd5e4eb39111d8e296c6b6baa5fe3ceb813254a67eec572f54a84ea`  
		Last Modified: Thu, 05 Feb 2026 00:17:19 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40531e11108828aad582e7afc2edf59972bf624c3a20172d4f96703a924229db`  
		Last Modified: Thu, 05 Feb 2026 00:17:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5544008d0cad5d6f0065be0d9aa0a8c3fb982b3a44822524271bffb38ba99860`  
		Last Modified: Thu, 05 Feb 2026 00:17:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10466a0fa3c2b5805f7b8e6e43924f5a9a8ffbd235f02f4235181009bec002fb`  
		Last Modified: Thu, 05 Feb 2026 00:17:21 GMT  
		Size: 4.9 KB (4894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356c39a5b7a996f9a7c1429f605e8069379152e94666e3b1814f9dac5e96a13a`  
		Last Modified: Thu, 05 Feb 2026 00:17:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e963d10a90cb0da8729043cfe28b2d36bb6b25a23a7f02aa3baed02ccb49c780`  
		Last Modified: Thu, 05 Feb 2026 00:17:22 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234c6992c2f570dd2da3331d2ff34eb4dae7570c7bcef641077c2630da60a38b`  
		Last Modified: Thu, 05 Feb 2026 00:17:22 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8a51c3b525bff655d3df997d2534cf8a34a0036a408c4e440aba9d073fdbef`  
		Last Modified: Thu, 05 Feb 2026 00:17:23 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.5` - unknown; unknown

```console
$ docker pull kibana@sha256:bcb752ca6e467ac0f959629e436d2a814cd2df1045829658c38cd86d2ce62e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c7c1217d5092f99764092a1519c287e91f9bfd81ea026c461f085afd610fe1`

```dockerfile
```

-	Layers:
	-	`sha256:d57277aedeb974c95c72b5a7465a35d2c1f88aae90426a2bfdcc724930a9f114`  
		Last Modified: Thu, 05 Feb 2026 00:17:19 GMT  
		Size: 5.7 MB (5746261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d014ba10c4efa52852ef1c45d2acba207b1c597da6074d8600b2d24bb449cdb`  
		Last Modified: Thu, 05 Feb 2026 00:17:18 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.0`

```console
$ docker pull kibana@sha256:549ef86c3dcf80edeec41863ebc9a41e26cd32bc6bef0bc2ce9fe2ff74546b05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.0` - linux; amd64

```console
$ docker pull kibana@sha256:3d6433e6ef9326db9b7b3005e78e278548a1fd49bf3f1f0aba4eec6617449414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.8 MB (453840941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba0417f3bd6aa8da25acb7e0ddffe2f4e954dc367c69460094ac18735004f0b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:09:03 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 00:09:03 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:18:03 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 00:18:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:18:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 00:18:04 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 00:18:04 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 00:18:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 00:18:04 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:18:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:18:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 00:18:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:18:05 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 00:18:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 00:18:06 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 00:18:06 GMT
LABEL org.label-schema.build-date=2026-01-29T09:38:21.004Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=30ab63cc0017fe2da7a84fb9b285dd762468802d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T09:38:21.004Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=30ab63cc0017fe2da7a84fb9b285dd762468802d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Thu, 05 Feb 2026 00:18:06 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 00:18:06 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:18:06 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 00:18:06 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 00:18:06 GMT
USER 1000
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4bee95e444c92a3d9c0fc417f2dffbf03b3eed7b2b1d82c361f08b9067da7e`  
		Last Modified: Thu, 05 Feb 2026 00:19:00 GMT  
		Size: 19.5 MB (19531073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41a824949582a0d9ab529c3c3e0b98305272706f21c71bbd35c1e48b53fcb39`  
		Last Modified: Thu, 05 Feb 2026 00:19:08 GMT  
		Size: 377.7 MB (377742393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fba42f740f092fa2d7100f58d8e2f7e794cc7970384cc7f36cbe84543190427`  
		Last Modified: Thu, 05 Feb 2026 00:18:59 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee2748f6edefd5dcb805bcd5db00ed628a9a3aeff43b8aff2e4035259f2a46f`  
		Last Modified: Thu, 05 Feb 2026 00:19:00 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b167a05e310442d74fed3e159286947c50574ee51cb275d527f93e90e9422bb1`  
		Last Modified: Thu, 05 Feb 2026 00:19:00 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe3c0de0dad3b0c156ccec86c624f2739f3daaec91cb78df6aca7680eeb9df1`  
		Last Modified: Thu, 05 Feb 2026 00:19:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4bcef81f16a7069bfea0ad70f293d46d6ba1253c5f88b175e5770fe49d22f0`  
		Last Modified: Thu, 05 Feb 2026 00:19:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe2721d248acdc88a5825593f841e8ca3e96df11b1dab1b33cee23a84a88d77`  
		Last Modified: Thu, 05 Feb 2026 00:19:02 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ef21e538162ec78fe760837d2659a1d44fa84377000d4630798ad3595ccff3`  
		Last Modified: Thu, 05 Feb 2026 00:19:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef94141d6333757b86649734bd336a48d884d741123a04e05d8ebf0701f5b66`  
		Last Modified: Thu, 05 Feb 2026 00:19:03 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa7244c417630ef6cfac98d0b6b5930ccc7f5fbe8f0d854fc5a2cc84a799d5`  
		Last Modified: Thu, 05 Feb 2026 00:19:03 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc967f476a012e5a57610ce7d1090bc7de7df98fe96caf0b6e8e3a3052e3db36`  
		Last Modified: Thu, 05 Feb 2026 00:19:04 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.0` - unknown; unknown

```console
$ docker pull kibana@sha256:571b56ef1304f205e11cb68a6508287ed6782ecb0773e40a5f0dc4443abfb213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694a6591347c191207b8fc212b0fb2274172afd927036e65979dfd3cf4022e46`

```dockerfile
```

-	Layers:
	-	`sha256:e28207d56806b37af42ad3d9d6a0eb32740cf2b02b24c166b64556ec2580d862`  
		Last Modified: Thu, 05 Feb 2026 00:18:59 GMT  
		Size: 5.8 MB (5813708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:439fe36470b7095069f62aab5c988c79f98edd25fc8ea7115b4c42351493d663`  
		Last Modified: Thu, 05 Feb 2026 00:18:59 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:bc39658e21fd2dedea0b3af05469f02d6a0448b4ae6c0863ef000b4885309924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.7 MB (465703579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452f6047766a8ea412b86b96de8fd8e8cb2ad1a47e570f6dbb0b870e4b43baec`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:08:36 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Feb 2026 00:08:36 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:16:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Feb 2026 00:16:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Feb 2026 00:16:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Feb 2026 00:16:27 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Feb 2026 00:16:27 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Feb 2026 00:16:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Feb 2026 00:16:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Feb 2026 00:16:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:16:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Feb 2026 00:16:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 00:16:28 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Feb 2026 00:16:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Feb 2026 00:16:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Feb 2026 00:16:29 GMT
LABEL org.label-schema.build-date=2026-01-29T09:38:21.004Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=30ab63cc0017fe2da7a84fb9b285dd762468802d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T09:38:21.004Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=30ab63cc0017fe2da7a84fb9b285dd762468802d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Thu, 05 Feb 2026 00:16:29 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 05 Feb 2026 00:16:30 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 05 Feb 2026 00:16:30 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Feb 2026 00:16:30 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Feb 2026 00:16:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddd65ea46b160990c1a024dbdd1b3b5618a4645b6d9d6f366d1bed78ada2fd9`  
		Last Modified: Thu, 05 Feb 2026 00:17:35 GMT  
		Size: 19.5 MB (19481706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73c8b50d527fc5b19240a1778500a591b7d453e1538b6c7145887201b2f1cc`  
		Last Modified: Thu, 05 Feb 2026 00:17:42 GMT  
		Size: 391.5 MB (391469259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5ef88107e615dbae8bcd759f021f66f697f1ce528ae2356a20cc28cf53dead`  
		Last Modified: Thu, 05 Feb 2026 00:17:34 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff5a644b3b6fcdb14de198f13d42adbac12ae14e00b91528ff756f30ca8b3`  
		Last Modified: Thu, 05 Feb 2026 00:17:35 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c30a2b4daafa40641508871cdcff4d689c7430fd4b9baf2de3b2346ae5e74`  
		Last Modified: Thu, 05 Feb 2026 00:17:35 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96222161e5580a3e090383477a1fb547f501264807d7acda991b08e7c7e6e5ec`  
		Last Modified: Thu, 05 Feb 2026 00:17:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413ed349eb414736e2cc4d94504879d4f10f3c3c405d1f79ecf9e24d0757a8b9`  
		Last Modified: Thu, 05 Feb 2026 00:17:37 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8667ebf49680a5714ac4e24d1ed6a46eafb5958a11e7d665a3650906351d144`  
		Last Modified: Thu, 05 Feb 2026 00:17:37 GMT  
		Size: 4.9 KB (4916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f7ea28535d0c6bbdc3a0cb0ff02e56ee5bf0d941242bba9ce204f1921b8b95`  
		Last Modified: Thu, 05 Feb 2026 00:17:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd7f90f448f2b5345e6ae3453fd329665a1a97ba3125ed1782e9929f7b2d843`  
		Last Modified: Thu, 05 Feb 2026 00:17:38 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb92c0d2f3e1b9e39ec75ccb411c51eaa016b3c149ec02896ce57217978ac37`  
		Last Modified: Thu, 05 Feb 2026 00:17:38 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834a054fb81c4d24809adcc74b73561f820a08a3828aa87401e92cadab010c03`  
		Last Modified: Thu, 05 Feb 2026 00:17:39 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.0` - unknown; unknown

```console
$ docker pull kibana@sha256:b0753d906e6beaf456273149f1b698585770494e97c0d959b0384a56a05eb118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae6bf807da62001b10ba25a4e5d053e9c2fe2ab78fabb0efdb39ccb41d3b59`

```dockerfile
```

-	Layers:
	-	`sha256:8e5512687a84565f342ace1deb225144f9015f0a33089a09b47c4454189eb4d4`  
		Last Modified: Thu, 05 Feb 2026 00:17:34 GMT  
		Size: 5.8 MB (5812380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1d96ea29b2d13ef62810436e64f4e99f229f3dd8dc9fc735ae3d1316f20b1d`  
		Last Modified: Thu, 05 Feb 2026 00:17:34 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
