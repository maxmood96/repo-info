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
$ docker pull elasticsearch@sha256:98abaea1d231bd08c728bd6be2ccff416e236d946f16ce9e74a68007427aef64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6d9e08bcb60040adb42ba7058538c258cf50c0755d5f47fad74e8a1c2e37212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.6 MB (721609428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa224f0834bdd38a428e4d38955f55f009dd680b66f23bc0240ddad9142f816`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:45:15 GMT
ENV container oci
# Tue, 02 Jun 2026 05:45:16 GMT
COPY dir:089626db9f0e556d2460ea9b02a44cc63366766c2d8912a1fd05fdd542cbb8e4 in /      
# Tue, 02 Jun 2026 05:45:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:45:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:44:58Z" "org.opencontainers.image.created"="2026-06-02T05:44:58Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:44:58Z
# Tue, 02 Jun 2026 22:46:01 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:46:01 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Jun 2026 22:46:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:46:34 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 22:46:34 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Jun 2026 22:46:43 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Jun 2026 22:46:43 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Jun 2026 22:46:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:46:43 GMT
ENV SHELL=/bin/bash
# Tue, 02 Jun 2026 22:46:43 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:44 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Jun 2026 22:46:44 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Jun 2026 22:46:44 GMT
LABEL org.label-schema.build-date=2026-05-25T22:07:43.142271687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T22:07:43.142271687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Tue, 02 Jun 2026 22:46:44 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Jun 2026 22:46:44 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Jun 2026 22:46:44 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:46:44 GMT
CMD ["eswrapper"]
# Tue, 02 Jun 2026 22:46:44 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deab620ec2eb4e00e8dd3358a5ef3439e64ef4cb6506fccc1b75e9de6e9cd3e4`  
		Last Modified: Tue, 02 Jun 2026 22:47:36 GMT  
		Size: 4.1 MB (4115298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f9a348b3e359dc62e892304207da178d5a95c6956a21434f28fc7c18e53c87`  
		Last Modified: Tue, 02 Jun 2026 22:47:36 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbcec72f320e318677481b82c7504dda93d80f56d3de8c3cc7925b99e53baaf`  
		Last Modified: Tue, 02 Jun 2026 22:47:36 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c749ec02ad200a894a957224c3eea640d756b3c98036101c23c74cc1417fce4f`  
		Last Modified: Tue, 02 Jun 2026 22:47:49 GMT  
		Size: 676.7 MB (676717133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973564b474d17a8b196f98d2dc2b8cfb08521d7af7fb02f41f19990f0bdca93e`  
		Last Modified: Tue, 02 Jun 2026 22:47:37 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e83a55111e9704beff2aa1887fb5e55fe96a733c85aee83d0a72f4b7a0f9e1`  
		Last Modified: Tue, 02 Jun 2026 22:47:37 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa533fffbb39668d2216c0d796dfa1af572225693d9a67ae3d7c594641ddb76`  
		Last Modified: Tue, 02 Jun 2026 22:47:38 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e575419cf0b1ab67726c6ef6efb51127237bf51e159580c6d346eca70bb765`  
		Last Modified: Tue, 02 Jun 2026 22:47:39 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:27e5ea84b6adee06e8b98330bdf253f8a696e6b8cba3b51b79a73388e3e10fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3933c46a3e21c2c9f89d7282e31ff6d345f6a2a2e4e41398ed28b8f044a50451`

```dockerfile
```

-	Layers:
	-	`sha256:8d5dbecff02498f350d252d7c538b4cbb0d940a17bff5254d1753cfa462d52d3`  
		Last Modified: Tue, 02 Jun 2026 22:47:36 GMT  
		Size: 2.1 MB (2088836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a1abc0e088adaafb20a5b1347eddad88523c1a31cc106e817d04689e3733187`  
		Last Modified: Tue, 02 Jun 2026 22:47:36 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d96213357111783d8bd4f0c32f6efe0433acd5b2a6a5df6c3df738ee88cc734d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565692098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146320c409858010af9a8c4804b9ba296f5f6112a84f8d88cda395061cfdc177`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:50 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:51 GMT
COPY dir:45e3b0db7c7574b63ad7ec3e8aa88c1c154d382f5d855d74a5a8b46ed379a850 in /      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:51 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:37Z" "org.opencontainers.image.created"="2026-06-02T05:43:37Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:37Z
# Tue, 02 Jun 2026 22:45:38 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:39 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Jun 2026 22:46:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:46:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 22:46:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Jun 2026 22:46:35 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:46:36 GMT
ENV SHELL=/bin/bash
# Tue, 02 Jun 2026 22:46:36 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Jun 2026 22:46:36 GMT
LABEL org.label-schema.build-date=2026-05-25T22:07:43.142271687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T22:07:43.142271687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=7dcc32bebba091844c0207f9dae8fda6c7d08542 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Tue, 02 Jun 2026 22:46:36 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Jun 2026 22:46:36 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Jun 2026 22:46:36 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:46:36 GMT
CMD ["eswrapper"]
# Tue, 02 Jun 2026 22:46:36 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe30f1acab3bd4ea0dc361bc6e7b812c7d7048dfa24434fd1ae3aca68f89e711`  
		Last Modified: Tue, 02 Jun 2026 22:47:14 GMT  
		Size: 4.1 MB (4119698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda11cd502571a85366681afcf44743cc3fe18b41e994df2aaa6e1498ddfa635`  
		Last Modified: Tue, 02 Jun 2026 22:47:13 GMT  
		Size: 1.5 KB (1538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b1421bc149ad21a780409dc2ba5ff27736b8bc7166bb6dd6e48ac0deed0e9f`  
		Last Modified: Tue, 02 Jun 2026 22:47:14 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b3a4c97d367b024883585d5117c13c68b1216a3bb7d660262da13947812d52`  
		Last Modified: Tue, 02 Jun 2026 22:47:24 GMT  
		Size: 522.6 MB (522620775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2d56dfe099a0b7766dd2c1dc3cc8f861edb4afcc365878b444f8b74e67ce40`  
		Last Modified: Tue, 02 Jun 2026 22:47:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5876dfe82433e51ef48fb97d8a1afe157e5eba42f3edaff6f0961c02eb045f74`  
		Last Modified: Tue, 02 Jun 2026 22:47:15 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce732f1b1eaeb8e8af1a10d21d8d59b678e26215342bc8994917f92a3a65c5f`  
		Last Modified: Tue, 02 Jun 2026 22:47:15 GMT  
		Size: 74.1 KB (74110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba479ef045cfda9440b358742395c0bcb57fd447f83d28705f352283b6817fd`  
		Last Modified: Tue, 02 Jun 2026 22:47:16 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c00e42a564e6348610d81b4b52b44f42f4318064f514c8a8db234127ca75e9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0123a9e9069e70183834539df90922b2139b02db7a038dff8e41913e7528cd16`

```dockerfile
```

-	Layers:
	-	`sha256:6fcf4494a28b7ddef7d8d977b889059ecc6345d532b3b1b9893e090dd0bc882c`  
		Last Modified: Tue, 02 Jun 2026 22:47:14 GMT  
		Size: 2.1 MB (2089398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc01eac773f0f1a75dfec540815b276f5e50c4df5ba58a26f88857fdcc1a668`  
		Last Modified: Tue, 02 Jun 2026 22:47:13 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.2`

```console
$ docker pull elasticsearch@sha256:5a2a64b3325fce8c82ea4f2f3d3955c93d7d34d96831fe475b45310da5c27fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3d747dcdcc025f00f99e4982c17073c3e672055a02abaf29c1e45b52d19adef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.1 MB (865110253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0019e98b2b3c03dc93a0d311fbc6d631ab496eebf71b080afad5d04ba0b54c38`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:45:15 GMT
ENV container oci
# Tue, 02 Jun 2026 05:45:16 GMT
COPY dir:089626db9f0e556d2460ea9b02a44cc63366766c2d8912a1fd05fdd542cbb8e4 in /      
# Tue, 02 Jun 2026 05:45:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:45:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:44:58Z" "org.opencontainers.image.created"="2026-06-02T05:44:58Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:44:58Z
# Tue, 02 Jun 2026 22:46:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:46:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Jun 2026 22:46:45 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:46:45 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 22:46:45 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Jun 2026 22:46:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Jun 2026 22:46:56 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Jun 2026 22:46:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:46:56 GMT
ENV SHELL=/bin/bash
# Tue, 02 Jun 2026 22:46:56 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:56 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Jun 2026 22:46:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Jun 2026 22:46:56 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Tue, 02 Jun 2026 22:46:56 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Jun 2026 22:46:56 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Jun 2026 22:46:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:46:56 GMT
CMD ["eswrapper"]
# Tue, 02 Jun 2026 22:46:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b71bd3a30cadf9a3f2e8c9daa659bb7d3aaa45634caa2220471b07bd00a5e`  
		Last Modified: Tue, 02 Jun 2026 22:47:50 GMT  
		Size: 4.1 MB (4115227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bda7360fabab7b992cbaff2f3ddb7ff609503322004ddadedb36d1c20f428b4`  
		Last Modified: Tue, 02 Jun 2026 22:47:50 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560bc1042bff20f73d364b3fa25ab8c631e64b2a0945f655ce89c3cd86487023`  
		Last Modified: Tue, 02 Jun 2026 22:47:50 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5912b704198e4714de0cc5cbf397ef8a1f283bd939b6c8810a8e25f33dd3f8e2`  
		Last Modified: Tue, 02 Jun 2026 22:48:12 GMT  
		Size: 820.2 MB (820218027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0624cdd50b2c1e06f10f2b2550780cf991e4f7c8ba72e951bac9cd84b30e2c49`  
		Last Modified: Tue, 02 Jun 2026 22:47:52 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52387eb0404f602747d6de3dc79549a346ac81dd318d02e8f780703e937a9001`  
		Last Modified: Tue, 02 Jun 2026 22:47:52 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec61f0f1ff5dadac1ee663c98dc169256bae5594820084836605ece3e7d4741`  
		Last Modified: Tue, 02 Jun 2026 22:47:52 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de1bf066987b75c3ff0babf9ad4e058453cc01e8330408adbfd84ef35913043`  
		Last Modified: Tue, 02 Jun 2026 22:47:53 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:83306c4ed1c559a4ad96de4f9c7d1065d977ff181710f9109daa4438e8f2806e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334d4618bc9c40b65f3647485b61695cffd9adfb5ada9445a5b8af5c0eb5e04c`

```dockerfile
```

-	Layers:
	-	`sha256:97a9a30eafea389e874f6b6037fdd07dd5bbffa7e7d5869826a7b88482ee2931`  
		Last Modified: Tue, 02 Jun 2026 22:47:51 GMT  
		Size: 2.4 MB (2391021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e56b2abd80b0ea9be910ff6803863e76d00359a3d92dce4d9ef5492a5da0b30f`  
		Last Modified: Tue, 02 Jun 2026 22:47:50 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:8333ef1bd8d735cd3852292adcf85f70b6442187d574ab89bdfb55a9702584dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709769399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30769389b39420d804d923859b97d9aed809f6b238cc390c9c960107a0ae81fb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:50 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:51 GMT
COPY dir:45e3b0db7c7574b63ad7ec3e8aa88c1c154d382f5d855d74a5a8b46ed379a850 in /      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:51 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:37Z" "org.opencontainers.image.created"="2026-06-02T05:43:37Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:37Z
# Tue, 02 Jun 2026 22:45:35 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:35 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Jun 2026 22:46:38 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:46:38 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 22:46:38 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Jun 2026 22:46:46 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Jun 2026 22:46:46 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Jun 2026 22:46:46 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:46:46 GMT
ENV SHELL=/bin/bash
# Tue, 02 Jun 2026 22:46:46 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:46 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Jun 2026 22:46:46 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Jun 2026 22:46:46 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:36.017759931Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T22:10:36.017759931Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c402c2b36d90eae29c0182f86bd9050fd0b746cc org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Tue, 02 Jun 2026 22:46:46 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Jun 2026 22:46:46 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Jun 2026 22:46:46 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 22:46:46 GMT
CMD ["eswrapper"]
# Tue, 02 Jun 2026 22:46:46 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4d7c5e8cdae16c0b90d8bdca63e80a6e80668c4da305d2ba86f7fa1b018f3b`  
		Last Modified: Tue, 02 Jun 2026 22:47:33 GMT  
		Size: 4.1 MB (4119697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892e3b8d6c97b2aba7d0819e8fe2f79580456147e1e18242fc5c811de03856e8`  
		Last Modified: Tue, 02 Jun 2026 22:47:32 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c77134732b48278b4a611f06d77259e8701209e199e031ffb788fffbb59522`  
		Last Modified: Tue, 02 Jun 2026 22:47:33 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b160340a208ff79b7d00a2b6ca54cad9212ad3315c8a50807a6f80f08edb46f`  
		Last Modified: Tue, 02 Jun 2026 22:47:45 GMT  
		Size: 666.7 MB (666698102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd301a6b72f594906eb9bf0308b8a897811680760e02baeb63a984ceb0465eb`  
		Last Modified: Tue, 02 Jun 2026 22:47:34 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaf1927a49be485df09d078d36ac058129144da1c43562a9d510c50041980e5`  
		Last Modified: Tue, 02 Jun 2026 22:47:34 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7333bd7c7ca8ae41e7502b0494747e5670f7e43e2a7b4a637804388114ec49f`  
		Last Modified: Tue, 02 Jun 2026 22:47:34 GMT  
		Size: 74.1 KB (74104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cb28dd40eca9217cc5223ce6150ddb2f86c92d9865a456771cde788d0e13a1`  
		Last Modified: Tue, 02 Jun 2026 22:47:35 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d7e894bff22c231542cdbd01ce7a05f3cc31347b9c87089f529ee0b3b5343a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2425541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3dbc1d9beb696605b310503ea9108a36584515ce74fac801347c4c8029b0307`

```dockerfile
```

-	Layers:
	-	`sha256:708b59154ba4382586a5e555d57793f8dfe2ae962e12f66e8875c259012e34b8`  
		Last Modified: Tue, 02 Jun 2026 22:47:33 GMT  
		Size: 2.4 MB (2391583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c84033ac02d81112e050c6fdee46a8f9c6c085431589ee829e305aae0c95a53`  
		Last Modified: Tue, 02 Jun 2026 22:47:32 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json
