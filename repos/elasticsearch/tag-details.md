<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.16`](#elasticsearch81916)
-	[`elasticsearch:9.3.5`](#elasticsearch935)
-	[`elasticsearch:9.4.2`](#elasticsearch942)

## `elasticsearch:8.19.16`

```console
$ docker pull elasticsearch@sha256:1560707af70542cbf59f4e7c5f06662fe81d18d476013f735f150c9cb3205d9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.16` - linux; amd64

```console
$ docker pull elasticsearch@sha256:282dfd2141199ef3336de829900c0ef1de965b3fcbeade837e299059ceab63a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.1 MB (721114742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58347d2b0d5c6dadd899edcdefb78d21866953700083f36cab77780ee24c5a2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:27 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 02 Jun 2026 08:15:27 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Jun 2026 08:15:27 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 08:15:27 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Jun 2026 08:16:06 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 02 Jun 2026 08:16:06 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 08:16:06 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:06 GMT
ENV SHELL=/bin/bash
# Tue, 02 Jun 2026 08:16:06 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:06 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Jun 2026 08:16:06 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 02 Jun 2026 08:16:06 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 02 Jun 2026 08:16:06 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Jun 2026 08:16:06 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:50.658641519Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0ecfe314ed6ddebb736091bf37b3b6758209b73b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.16 org.opencontainers.image.created=2026-05-25T22:10:50.658641519Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0ecfe314ed6ddebb736091bf37b3b6758209b73b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.16
# Tue, 02 Jun 2026 08:16:06 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:16:06 GMT
CMD ["eswrapper"]
# Tue, 02 Jun 2026 08:16:06 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aa0352c7bf6974450146647e1fc6dc4899474272e82e48eba6c6df928376f0`  
		Last Modified: Tue, 02 Jun 2026 08:16:59 GMT  
		Size: 6.1 MB (6073137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f517b6fda09d6f1f650949f1e29102e031b4806f9091afa0414187d2b66c2e54`  
		Last Modified: Tue, 02 Jun 2026 08:16:59 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fe629fa23ca328c98a069410e832f6ad0d7691fa0cf1469312dfc03ad2b463`  
		Last Modified: Tue, 02 Jun 2026 08:17:14 GMT  
		Size: 685.0 MB (685013854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ff446a91e94cfd35bd4b8e89b1049f8fd32d09306212e37d376505e42d3639`  
		Last Modified: Tue, 02 Jun 2026 08:16:59 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a5a069ada70251a942584e79c129c7a6911170c77ab27fec01be35f0f128a`  
		Last Modified: Tue, 02 Jun 2026 08:17:00 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac019e0d17877dcab3486f453fba8f46523e3b9486cb92d3e7dd34a9631fa71`  
		Last Modified: Tue, 02 Jun 2026 08:17:00 GMT  
		Size: 164.2 KB (164198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdacdcd3b44943a56e396c491b33e3eb024d45792131de8e480439200f7ed55`  
		Last Modified: Tue, 02 Jun 2026 08:17:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1372b53da523ef054617c28a4f4af3ba557eebdae07c437b0b0f940fdd28fe94`  
		Last Modified: Tue, 02 Jun 2026 08:17:02 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.16` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c4e7065bd034ab2671ae8a6bca1fc8e5c2236146ce26ca8a69301cc6e85f9909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3244133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a9fc1fd57541ce04cb8f3e6be55a2ea006e020a1a948fb21f834741e71fd2b`

```dockerfile
```

-	Layers:
	-	`sha256:328995a6e7e41acef69d3e6d19e6b9fb73693e842a741897dd90fc4aee605570`  
		Last Modified: Tue, 02 Jun 2026 08:16:59 GMT  
		Size: 3.2 MB (3207317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125852eec51b3d4411605cc3e1d9ad01011b71cc9fb693bac83738f6731c7efd`  
		Last Modified: Tue, 02 Jun 2026 08:16:59 GMT  
		Size: 36.8 KB (36816 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.16` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:fcbbb0a32c84ecb3fa3857953e7cbcee0268d9b962ec59b987030797d19b8945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.9 MB (568939846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cbbfb79dfc5de57a3093060a78ee4f048d446839f9656814bed9302fda97db`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:38 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 02 Jun 2026 08:16:38 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Jun 2026 08:16:38 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 08:16:38 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Jun 2026 08:17:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 02 Jun 2026 08:17:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 08:17:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:17:47 GMT
ENV SHELL=/bin/bash
# Tue, 02 Jun 2026 08:17:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:17:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Jun 2026 08:17:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 02 Jun 2026 08:17:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 02 Jun 2026 08:17:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Jun 2026 08:17:47 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:50.658641519Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0ecfe314ed6ddebb736091bf37b3b6758209b73b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.16 org.opencontainers.image.created=2026-05-25T22:10:50.658641519Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0ecfe314ed6ddebb736091bf37b3b6758209b73b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.16
# Tue, 02 Jun 2026 08:17:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:17:47 GMT
CMD ["eswrapper"]
# Tue, 02 Jun 2026 08:17:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb26e6dbe8bb7c03e509a693dcdc8481cdf556df0b1ecec11f0181f7696a8fc`  
		Last Modified: Tue, 02 Jun 2026 08:18:26 GMT  
		Size: 6.0 MB (5958142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3662823382eb004bce83cc941724f282bf8bdee0fb97dd6ee96b73eec9a84a90`  
		Last Modified: Tue, 02 Jun 2026 08:18:25 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cc2a35078425d3c043035ee6dc1b19e053f60f768960f2a52ad6d9e03c9ab9`  
		Last Modified: Tue, 02 Jun 2026 08:18:38 GMT  
		Size: 533.8 MB (533814283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757ac6f59fc67e950c63e4c9fee645a7251fd6007c25e215102e8c87837aa0d1`  
		Last Modified: Tue, 02 Jun 2026 08:18:26 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80c02acf2ff5aa52239e57dbda914ff433f3e06de95b2014a5f546d2bd42244`  
		Last Modified: Tue, 02 Jun 2026 08:18:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b1d471e89d357e5aac2294a96950ebeea8c363ef9a8cfb25d16951ea0c2c20`  
		Last Modified: Tue, 02 Jun 2026 08:18:27 GMT  
		Size: 160.7 KB (160698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670c4ed98ab78e73b43fe9c3050930843c634b6ed7fcfac08c1b0165c1ff9b8c`  
		Last Modified: Tue, 02 Jun 2026 08:18:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8242bbf744534e61d22484470138ee7e35e89043e061706209d496f90f7ffdd0`  
		Last Modified: Tue, 02 Jun 2026 08:18:28 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.16` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:87b4568b1d5e5f4545daa5cfdd6abbd664a16d8c74dfb98661115355936accb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3244749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815073a2c51394a7ebd35b246684c9a4cbb53d8141bae0cb7c1cae3f44c07322`

```dockerfile
```

-	Layers:
	-	`sha256:8c75adc8b2f6e889aab5f78386ccced812b3eb32e0f00e4967ee47d2e9df6923`  
		Last Modified: Tue, 02 Jun 2026 08:18:26 GMT  
		Size: 3.2 MB (3207730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716c84abc37a7beaf364eda31b000940acf1bef8a59284a9f3eecfb6dcaf47d2`  
		Last Modified: Tue, 02 Jun 2026 08:18:26 GMT  
		Size: 37.0 KB (37019 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.5`

```console
$ docker pull elasticsearch@sha256:a239bded1c116401fb1c09db12396bf7363b96a546df4943a3c384611ae1fc3a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:bdbaba5f954697e0a8fde601dbd277ac9051a08c872b41af891d9e32fdd71986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.6 MB (721602560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cfe4eef1699e690b64fed99054e16585454982da7c814e128cff1d2b64f176`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:14:56 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 15 Jun 2026 23:15:21 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:15:21 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:15:21 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:15:31 GMT
ENV SHELL=/bin/bash
# Mon, 15 Jun 2026 23:15:31 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 15 Jun 2026 23:15:31 GMT
LABEL org.label-schema.build-date=2026-05-25T22:07:43.142271687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T22:07:43.142271687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Mon, 15 Jun 2026 23:15:31 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 15 Jun 2026 23:15:31 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:15:31 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:15:31 GMT
CMD ["eswrapper"]
# Mon, 15 Jun 2026 23:15:31 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747e761593c32e509cc86a417b48b4f65d14956c99348c0a526a8452149a58da`  
		Last Modified: Mon, 15 Jun 2026 23:16:23 GMT  
		Size: 4.1 MB (4115457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbba1dbf950863e7d0a0eb29de32ea73396cce3ade6226e1cbaf636968690de`  
		Last Modified: Mon, 15 Jun 2026 23:16:23 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb83444047ba1970a0169344115fd70764c16871d575a48f331ff42c586ba75d`  
		Last Modified: Mon, 15 Jun 2026 23:16:23 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e1433d7398b764fa0ab762545158b6b3a1c96a5d96f4d888f4f9b4c3aa6799`  
		Last Modified: Mon, 15 Jun 2026 23:16:37 GMT  
		Size: 676.7 MB (676716952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49efe1bb08473e240a82bf588f6d4e5be8dab1deb6cd8d0d2dab76a4314d5687`  
		Last Modified: Mon, 15 Jun 2026 23:16:24 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0d246a4cc9f3304347c8746c42d568a8461a34c655de73af0ff92bc27296b5`  
		Last Modified: Mon, 15 Jun 2026 23:16:25 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fee9f0a17011de43e9a8c9d86bb2c3666bee48da978ef2adf1d23859e5be4b`  
		Last Modified: Mon, 15 Jun 2026 23:16:25 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687de919a8eab96137408f7c7fa52149af4c3526f75d4c2eefef4dcaac5e5e91`  
		Last Modified: Mon, 15 Jun 2026 23:16:26 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b6246e7d3a88c498b6539cc7f7c2a0c837cf413961299b55ddf334ea5f724da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a0cc627f2384628b00bde96f1c2e79fca6918c74f381fca985ee3bf633872a`

```dockerfile
```

-	Layers:
	-	`sha256:007093c9b573d05494183a9ef67a3372621666e36288de126377174777085fc3`  
		Last Modified: Mon, 15 Jun 2026 23:16:23 GMT  
		Size: 2.1 MB (2088840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5989a9a331baac4bb4f85bd73237f4407268f1896e385c6fa96aa849811c67a`  
		Last Modified: Mon, 15 Jun 2026 23:16:23 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:5f1a467e0cf475efe3298bfb12c289bf84648f4bc731374f1419cd3c399e3740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565702926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5144750795fa15a3ea9f81e93769aa02753d2cf04828402e1a7372cc2c3dc29`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:14:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 15 Jun 2026 23:15:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:15:19 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:15:19 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 15 Jun 2026 23:15:25 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 15 Jun 2026 23:15:25 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 15 Jun 2026 23:15:25 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:15:25 GMT
ENV SHELL=/bin/bash
# Mon, 15 Jun 2026 23:15:25 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:15:25 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 15 Jun 2026 23:15:25 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 15 Jun 2026 23:15:25 GMT
LABEL org.label-schema.build-date=2026-05-25T22:07:43.142271687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T22:07:43.142271687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Mon, 15 Jun 2026 23:15:25 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 15 Jun 2026 23:15:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:15:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:15:25 GMT
CMD ["eswrapper"]
# Mon, 15 Jun 2026 23:15:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52ae237b5846da10703c39acefd4761501438a780cec810e0c0ddde2a8e386d`  
		Last Modified: Mon, 15 Jun 2026 23:16:04 GMT  
		Size: 4.1 MB (4120788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfda81d76be7abcd2ed5efc76b759d20ea173ce0496e50851d98f39d8656a99`  
		Last Modified: Mon, 15 Jun 2026 23:16:04 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969b37ac39fed87e9f6365cab4d15f78ae420a0e25efec4c62803a48488e9f9e`  
		Last Modified: Mon, 15 Jun 2026 23:16:04 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abb51e6a873d191218b889d3acd83daebf6485cf51eea384f81144b8e0ee41c`  
		Last Modified: Mon, 15 Jun 2026 23:16:26 GMT  
		Size: 522.6 MB (522620657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bd577e5e3b52162653fce753b009a3341e7c13a788cb7c553101d59f2b0001`  
		Last Modified: Mon, 15 Jun 2026 23:16:05 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9490802408985c02bd11e8748754f516938e488ecfba6f2b46e3b59442a8081`  
		Last Modified: Mon, 15 Jun 2026 23:16:05 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2668424e5e32f616c7734e5480db6b91f1cccd5b12039b257b8c7c839e77f6`  
		Last Modified: Mon, 15 Jun 2026 23:16:06 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f13f9830bc3a402f0ee7bd0724f3c20e5c9c2411dfa04ea64145df7dcce473`  
		Last Modified: Mon, 15 Jun 2026 23:16:07 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:48b4024258e4ceff50793096c5905c8ccccfb77b63be6fecf8eec8125f797ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c78f4334959cc8df5e70e7b7697a3c7278775e908f509ce210fa16d45ca7963`

```dockerfile
```

-	Layers:
	-	`sha256:abe4c1677c80f42ec3e9325b4af20fd7e1ab4577b8f5ab235e896f34697cd28e`  
		Last Modified: Mon, 15 Jun 2026 23:16:04 GMT  
		Size: 2.1 MB (2089402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d89486d0c6795ae002af249a0070c508c5b5076f6622fc0df5f3cc983172fdc`  
		Last Modified: Mon, 15 Jun 2026 23:16:04 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.2`

```console
$ docker pull elasticsearch@sha256:715c5d552328d83dcee6082bd5125327332a649f8e0aedb5fe0553d7be75bf21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6d35c4030bcbfb93e50bd792f0e47d8364d3acb877d841f97195e4a110cf841c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 MB (865103528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591cd0e2ee8ca7a65e8a5fbcc495dea72ee69ed3ad4dd9405cfac7cac6d8c7c7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:14:56 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 15 Jun 2026 23:16:20 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:16:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:16:20 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 15 Jun 2026 23:16:31 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 15 Jun 2026 23:16:31 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 15 Jun 2026 23:16:31 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:16:31 GMT
ENV SHELL=/bin/bash
# Mon, 15 Jun 2026 23:16:31 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:16:32 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 15 Jun 2026 23:16:32 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 15 Jun 2026 23:16:32 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Mon, 15 Jun 2026 23:16:32 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 15 Jun 2026 23:16:32 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:16:32 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:16:32 GMT
CMD ["eswrapper"]
# Mon, 15 Jun 2026 23:16:32 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cee6e5935d0f06fb2a2455cd614e34acc4b7160a12e3a58b808b268e2565d6`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 4.1 MB (4115496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbba1dbf950863e7d0a0eb29de32ea73396cce3ade6226e1cbaf636968690de`  
		Last Modified: Mon, 15 Jun 2026 23:16:23 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd7042f59b372fb4abc5d83db83bfa8af7770b21f2129f00bc09c35e188adb3`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0010da65571dbff9324067c7a1b52f2fe917942a69f772b8834ba3ed8c6834ed`  
		Last Modified: Mon, 15 Jun 2026 23:17:42 GMT  
		Size: 820.2 MB (820217877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e999231bb3ed2836a60a193d1aaa6d778394327b3787ed69739baeb513630e`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a60cf00dcb96ab3080d7257aa943a7dc7fd051c32c85087ae87a1a80f904c0a`  
		Last Modified: Mon, 15 Jun 2026 23:17:28 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde4b69228720cd51da5f35484dbc36a70f12b4fdbc7294a24a5581bb807e4a2`  
		Last Modified: Mon, 15 Jun 2026 23:17:29 GMT  
		Size: 75.2 KB (75186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f039a9722a5dc5dc7d14eac04c8ef64e99ccda5639818fd31bd7731302f1be`  
		Last Modified: Mon, 15 Jun 2026 23:17:29 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3b872df0dd4450dadc8c7adb15ba02633489797efc87bf2dbed6adbc21fef085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbf79d8c0d425c13f74e0a0540b05d461de1d46e909fc7bf19d6d191a50e3a4`

```dockerfile
```

-	Layers:
	-	`sha256:aea72a5ec5e6c14e8e3bfa5a31ec4f5bd3dd7f925f964da4df2fe80726369ce0`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 2.4 MB (2391025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38de8bba6bb5a882aad927cd2e8e399526946fda882d8c3fa89fb30025ce5298`  
		Last Modified: Mon, 15 Jun 2026 23:17:27 GMT  
		Size: 33.8 KB (33775 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:1c6d34f48b8da99c13ab7211fa050274ee0f4bbbec72e88cc87ba14a05a0086e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709780121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916060414839765b3c5334fc653ac7c46418e086cca1c4a193579d3ece6feb42`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:14:22 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:22 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 15 Jun 2026 23:15:33 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:15:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:15:33 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 15 Jun 2026 23:15:40 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 15 Jun 2026 23:15:40 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 15 Jun 2026 23:15:40 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:15:40 GMT
ENV SHELL=/bin/bash
# Mon, 15 Jun 2026 23:15:40 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:15:41 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 15 Jun 2026 23:15:41 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 15 Jun 2026 23:15:41 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Mon, 15 Jun 2026 23:15:41 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 15 Jun 2026 23:15:41 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:15:41 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 15 Jun 2026 23:15:41 GMT
CMD ["eswrapper"]
# Mon, 15 Jun 2026 23:15:41 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8cec1af2b18d221ffb16e0c6e868eb74dc2837b1ce5c301a634033ec179137`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 4.1 MB (4120762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b8276c57878e1868c3d80c94f03815f0e4d2e41c23c1316cde25a2f912b63`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5a991ca15efcc9f28e063a853a65f5a651eb3cf8c27d02b709873e1643a6a6`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87da9774d1d8d47717cf41d310f8d01606951b8f9d334033cb24b96b189e427`  
		Last Modified: Mon, 15 Jun 2026 23:16:42 GMT  
		Size: 666.7 MB (666697876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236e72258713ca2820a7fb631b0e062b52f745734faee20bcbbb8835cc3244b`  
		Last Modified: Mon, 15 Jun 2026 23:16:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f392cbca88ae4b3400b69e45137975e11de8d0191dccbdb6ceaa01337573c2aa`  
		Last Modified: Mon, 15 Jun 2026 23:16:28 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987ee265a78474021b0dc187aae5303f67f7285eb736badb60224ff17813b93`  
		Last Modified: Mon, 15 Jun 2026 23:16:29 GMT  
		Size: 74.1 KB (74109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2de42610097dca4fad2d7a0cd14cdc6f7be2ce5ba5a8c02f3ef23e99cdc948c`  
		Last Modified: Mon, 15 Jun 2026 23:16:30 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e2d9015034855aa00f21ce0cd03a53c71df1732d7185035a459a6570e6ae7222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba7561a47a030f51e709220a5b91b8d1b066f3f5eed916a600f444c2f26898b`

```dockerfile
```

-	Layers:
	-	`sha256:47b63c368795dc5ca2dc6e743c4e66dc364a9211e8c83134d84661a3f801777c`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 2.4 MB (2391587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae39a38e853d468054224d8f8bc96f65be769bcc2e0fea326218ea9a509d6dcf`  
		Last Modified: Mon, 15 Jun 2026 23:16:27 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json
