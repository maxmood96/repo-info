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
$ docker pull elasticsearch@sha256:c572d7ce8c86a6043ebb2fb662c6daa6b83cb0d6b7b37eeee3ee8e0c44ed13c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:802f6d1396834bafd23662e5d14b1f0c1b43f777e6a4e9dc1c330dd4a1e50e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.6 MB (721631160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d15db9238767794623404c4c3092512fee177656f7709905bef9bee9a5006fa`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Thu, 28 May 2026 21:49:54 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 28 May 2026 21:49:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 May 2026 21:51:04 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:51:04 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:51:04 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2026 21:51:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 28 May 2026 21:51:13 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 28 May 2026 21:51:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:51:13 GMT
ENV SHELL=/bin/bash
# Thu, 28 May 2026 21:51:13 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 May 2026 21:51:13 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 May 2026 21:51:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 May 2026 21:51:13 GMT
LABEL org.label-schema.build-date=2026-05-25T22:07:43.142271687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T22:07:43.142271687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Thu, 28 May 2026 21:51:13 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 28 May 2026 21:51:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 28 May 2026 21:51:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2026 21:51:14 GMT
CMD ["eswrapper"]
# Thu, 28 May 2026 21:51:14 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a5338672c26bb857e2808381df62a3101d827d97697537295919809a886be4`  
		Last Modified: Thu, 28 May 2026 21:52:04 GMT  
		Size: 4.1 MB (4115476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea62f7e85c938b869e09498093f2b04d3a8acb9cf6e34cd35958ab2ad8fd64f`  
		Last Modified: Thu, 28 May 2026 21:52:03 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1890d329c0c4c9428a1679ebdf0979e26c5ea832d903d985e6df605ee78e85a6`  
		Last Modified: Thu, 28 May 2026 21:52:03 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aed52952e0c15270dbaebf0abde96e25963b72349d4d99f23d56d55432b24b6`  
		Last Modified: Thu, 28 May 2026 21:52:16 GMT  
		Size: 676.7 MB (676717027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459b3b491094a265283584ddd26e010170690f3be92a1343fb142c594b0d5466`  
		Last Modified: Thu, 28 May 2026 21:52:04 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436e402d6d3bbc6d785971613a7756f9122cd9c492f741c7b598b1fb98673851`  
		Last Modified: Thu, 28 May 2026 21:52:05 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49c14065e0806f72e5c2ae7a363b2334dc30921e5c4ecb9625188d437c1cf09`  
		Last Modified: Thu, 28 May 2026 21:52:05 GMT  
		Size: 75.2 KB (75185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21e06aaa9d77612797b184b6e6343f4902b8f48b9feb318c902f6e00f5aecd4`  
		Last Modified: Thu, 28 May 2026 21:52:06 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:beff67021346c22cfa1800e4b4ddd26c909d50257b66943704b09d644cade04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3345b4a24b6ad0ea653bc78102ac6fea1c4605f6ca627524ea80a90029cfec4b`

```dockerfile
```

-	Layers:
	-	`sha256:510be51081a319336b89b0c8ec08412076f9302adda2a1785024f580c0ea1936`  
		Last Modified: Thu, 28 May 2026 21:52:03 GMT  
		Size: 2.1 MB (2088836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7376769b34725dc60c6b533a70fcdc12db6c8ce0621c71ef191485858da99f6`  
		Last Modified: Thu, 28 May 2026 21:52:03 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:94a4c524dfb1e480e60e063b56d343b2a0b0458f9ab555040983caede88d03fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565670338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b148a57aafa26ba9f62cb75a4e043d7900852658e59066e31f99faa07d590df`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Thu, 28 May 2026 21:33:50 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 28 May 2026 21:33:50 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 May 2026 21:34:21 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:34:21 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:34:21 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2026 21:34:27 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 28 May 2026 21:34:28 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 28 May 2026 21:34:28 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:34:28 GMT
ENV SHELL=/bin/bash
# Thu, 28 May 2026 21:34:28 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 May 2026 21:34:28 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 May 2026 21:34:28 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 May 2026 21:34:28 GMT
LABEL org.label-schema.build-date=2026-05-25T22:07:43.142271687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T22:07:43.142271687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Thu, 28 May 2026 21:34:28 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 28 May 2026 21:34:28 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 28 May 2026 21:34:28 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2026 21:34:28 GMT
CMD ["eswrapper"]
# Thu, 28 May 2026 21:34:28 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfe629b849cf123d1f7840c5267040af60937526384f5a73486a7cbfe802b9b`  
		Last Modified: Thu, 28 May 2026 21:35:06 GMT  
		Size: 4.1 MB (4120852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7565b2901e9c484c54758fa75a4782546fc7ca74eaa322eb97d69bf7254cd3`  
		Last Modified: Thu, 28 May 2026 21:35:06 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a48b216bd6b069ef28a2c3c7abffd54635d530e46467a1b9cd4d19060251c7`  
		Last Modified: Thu, 28 May 2026 21:35:06 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895858e74adf37554a8d2083e2d69511191c95e45772714c8d244433ffea7c9c`  
		Last Modified: Thu, 28 May 2026 21:35:16 GMT  
		Size: 522.6 MB (522620871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e815bbd4fcb90d6ec9dd21eabc64680c0a8ee08a4ea413181f47611f8c335e18`  
		Last Modified: Thu, 28 May 2026 21:35:07 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb1b80008503753a8de27883973cbb6deb886d70f7c9ebdc8578de1864b0892`  
		Last Modified: Thu, 28 May 2026 21:35:08 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc451b7e38f41924bf46b1b62c546b375c5dd593f1a9e97a13e5cbf9f331425`  
		Last Modified: Thu, 28 May 2026 21:35:08 GMT  
		Size: 74.1 KB (74111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14224f5dea6dd52de6e75e23e4b96fd93fd0f2fdeb6862eafa5f83ad1a67792a`  
		Last Modified: Thu, 28 May 2026 21:35:09 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:bc90a1825ef91d5d95a991f64e2ff313b0b95a06f1e96d030c5dc22d82764a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2cc197c1f1b489eb5f37ac3627f8373773bbf2ba646a7b8c6ca794badf695e`

```dockerfile
```

-	Layers:
	-	`sha256:9a8645c26b1254e89d45a5fa0b3c7eaf38c50d8c0e88677f2d8280cbd4fc1063`  
		Last Modified: Thu, 28 May 2026 21:35:06 GMT  
		Size: 2.1 MB (2089398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92c73718603a631fbafa8932e75eba86ea9262e7c3a5ee271c9530df8ce8f5b`  
		Last Modified: Thu, 28 May 2026 21:35:06 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.2`

```console
$ docker pull elasticsearch@sha256:f5c2b9ae3fcc6bf976db587e47f1aaec66640cbf997a33fdd3a8ebc2fd287d47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:da2d93b7a1db27f4199fb711c86940d65d1376aabb13ecfc50463f1f57589a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 MB (865132311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004587e84e8f23926eb9ecd4427d4ff50d747a1d377469192cb5108f6db3eca2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Thu, 28 May 2026 21:34:45 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 28 May 2026 21:34:45 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 May 2026 21:35:35 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:35:35 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:35:35 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2026 21:35:46 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 28 May 2026 21:35:46 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 28 May 2026 21:35:46 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:35:46 GMT
ENV SHELL=/bin/bash
# Thu, 28 May 2026 21:35:46 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 May 2026 21:35:47 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 May 2026 21:35:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 May 2026 21:35:47 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Thu, 28 May 2026 21:35:47 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 28 May 2026 21:35:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 28 May 2026 21:35:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2026 21:35:47 GMT
CMD ["eswrapper"]
# Thu, 28 May 2026 21:35:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ee89241b47fee2179cb4e1c10f60042e75d8d2cf55348b6b9c7fb5c82f23`  
		Last Modified: Thu, 28 May 2026 21:36:45 GMT  
		Size: 4.1 MB (4115624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e50a9f3445ff1a70db6fc26c31c7745d5ca7cb17bdc0026e54f3c44c733ff`  
		Last Modified: Thu, 28 May 2026 21:36:45 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65e43ec7e3b17b5e36b89608dac07a6344ddedf706a8abe74f96ce200daba04`  
		Last Modified: Thu, 28 May 2026 21:36:45 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ddc62444e4d6c7145b730329f27502aed73ad5fb64c479c43d0be6a1befab1`  
		Last Modified: Thu, 28 May 2026 21:37:01 GMT  
		Size: 820.2 MB (820218025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242c27f386366025222c2f51b199ab19c7a06ab27bfae4b1633c9f193f4ba796`  
		Last Modified: Thu, 28 May 2026 21:36:47 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7d430e2b28214f8d6cfb3b47c0ba3a1df9071d49d34ba14cb2c92ab87aeb12`  
		Last Modified: Thu, 28 May 2026 21:36:46 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5dff3a21ac8c1b8a4df4cc01592e68ab70d47f0de08e70fdd2a794eda3407c`  
		Last Modified: Thu, 28 May 2026 21:36:47 GMT  
		Size: 75.2 KB (75189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3241ab903da2c430d7b04383fc8f90230f2415be8b733571a8ef3ca581fb825a`  
		Last Modified: Thu, 28 May 2026 21:36:48 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:70a66900cd07b391ddc16dc6bee6192456030c0d072be9d4a382ca6be6a26d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102df243c7a8e75c390f4ce530a5477a92af5478651edfc154b48d899da5f897`

```dockerfile
```

-	Layers:
	-	`sha256:73de775839018ea039fe66a8bf1c6e2832634da8d695462739a443fe948826be`  
		Last Modified: Thu, 28 May 2026 21:36:45 GMT  
		Size: 2.4 MB (2391021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a25f13eca903a7cab3ed54aa735c9e537ab7f9d6793743a291fcc09bb6743e`  
		Last Modified: Thu, 28 May 2026 21:36:45 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:409e6ccd26535ea862e02d9eea4221dd7606ebea673852450016fb17fbcf3383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.7 MB (709747346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336025ac5c6db5605cf25f375d58d04d72d15613692669916bc875c2aae0b39b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Thu, 28 May 2026 21:34:11 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 28 May 2026 21:34:11 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 May 2026 21:34:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:34:47 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:34:47 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2026 21:34:55 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 28 May 2026 21:34:55 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 28 May 2026 21:34:55 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:34:55 GMT
ENV SHELL=/bin/bash
# Thu, 28 May 2026 21:34:55 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 May 2026 21:34:55 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 May 2026 21:34:55 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 May 2026 21:34:55 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Thu, 28 May 2026 21:34:55 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 28 May 2026 21:34:55 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 28 May 2026 21:34:55 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2026 21:34:55 GMT
CMD ["eswrapper"]
# Thu, 28 May 2026 21:34:55 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6651fcee88aa870199675fd385db5df2d9c077163db47f2ec0d9cdb7fcff19`  
		Last Modified: Thu, 28 May 2026 21:35:41 GMT  
		Size: 4.1 MB (4120854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbd0f0420fd5ab568783175a00be55301e77c0a67f890235058c70893e545de`  
		Last Modified: Thu, 28 May 2026 21:35:41 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cd04f6d8d3f62e75cceecbcdb774c4fd409336c8abb98b62225910921f66b`  
		Last Modified: Thu, 28 May 2026 21:35:41 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f337dad44c09d21a2121da8cc356eb8713fce99a0c9626d73aee86ee7bae374`  
		Last Modified: Thu, 28 May 2026 21:35:53 GMT  
		Size: 666.7 MB (666697883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056621edc95d392fbe926569b592a4dc8de68b37bd756bdbedccd29c4aa65d92`  
		Last Modified: Thu, 28 May 2026 21:35:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11fe6bdb673c292cb77ef44d778bc94c288dd344ec9fa317e3fbbcf930f83aa`  
		Last Modified: Thu, 28 May 2026 21:35:42 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecda1223ddc673040a882152f445795bd39e06b3087aa7f8fb763c205a2789c6`  
		Last Modified: Thu, 28 May 2026 21:35:42 GMT  
		Size: 74.1 KB (74106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb56076ee4e329520cca8dc543b58669522ca7f27a4402dbab3db42f94d9609`  
		Last Modified: Thu, 28 May 2026 21:35:43 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:fde580869366ca9836d96ae3ff12193cd1818d1ba945ce81b56066f7ba8c3a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cf1cbce527936a4119132d038fe6c58da7f5d2fb923a446200b7ffb200cf7a`

```dockerfile
```

-	Layers:
	-	`sha256:640398a7a4cb869ddd8c1f1534887bd8e5539a559610e9f2048fae295c9fcb87`  
		Last Modified: Thu, 28 May 2026 21:35:41 GMT  
		Size: 2.4 MB (2391583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2371ab3e35a9c6de486b496a0b7184a040e513484b310014d8fd9f36d59c5f0`  
		Last Modified: Thu, 28 May 2026 21:35:41 GMT  
		Size: 34.0 KB (33957 bytes)  
		MIME: application/vnd.in-toto+json
