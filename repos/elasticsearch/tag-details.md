<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.12`](#elasticsearch81912)
-	[`elasticsearch:9.2.6`](#elasticsearch926)
-	[`elasticsearch:9.3.1`](#elasticsearch931)

## `elasticsearch:8.19.12`

```console
$ docker pull elasticsearch@sha256:89729a95066a09a850ad307bcedaae1579403911c3e8880bee5162cd757ba09a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.12` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e57ccc8c21c14db2e26d7360cf42c503f915df1b40ad696b4ca6e99b9852be4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.2 MB (716189445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d7a1bac0a3d0b3424a7faa328f95e410378e620ceaaa6f72ac17df1822bdf3`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:23:41 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 17 Mar 2026 01:23:42 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 17 Mar 2026 01:23:42 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Mar 2026 01:23:42 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 17 Mar 2026 01:25:08 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 17 Mar 2026 01:25:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Mar 2026 01:25:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:25:08 GMT
ENV SHELL=/bin/bash
# Tue, 17 Mar 2026 01:25:08 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:25:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 17 Mar 2026 01:25:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Mar 2026 01:25:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Mar 2026 01:25:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 17 Mar 2026 01:25:09 GMT
LABEL org.label-schema.build-date=2026-02-23T23:08:40.713020893Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=840cd2a58b052d1632219ee0b8dcc0f364226287 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.12 org.opencontainers.image.created=2026-02-23T23:08:40.713020893Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=840cd2a58b052d1632219ee0b8dcc0f364226287 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.12
# Tue, 17 Mar 2026 01:25:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:25:09 GMT
CMD ["eswrapper"]
# Tue, 17 Mar 2026 01:25:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04d5100fedfae15138956758496e9b8c149916ea460cdf6b5d589ed6e23695c`  
		Last Modified: Tue, 17 Mar 2026 01:25:59 GMT  
		Size: 6.0 MB (5962734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a274355ce468380bd06d066a6251c450f6287d5efaa1364ecf8dbf0d2f6f8b4`  
		Last Modified: Tue, 17 Mar 2026 01:25:58 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b59465ca1dc6e1e7b938e52af03b2ef07615c9d09f642b8a6580017d64085e3`  
		Last Modified: Tue, 17 Mar 2026 01:26:11 GMT  
		Size: 680.2 MB (680199777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43769d62b592695e1dcb0c95b2ca7e07114bf56cd9d6567e6f9887f52b975ec5`  
		Last Modified: Tue, 17 Mar 2026 01:25:58 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ec9370b3b92b24e705263f30105c228550e5ded5d25e77c7b245ee2e6d41b9`  
		Last Modified: Tue, 17 Mar 2026 01:26:00 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a510f527bcf073377519f50c21ef4667a790c52c3f46077878f0851b240a1750`  
		Last Modified: Tue, 17 Mar 2026 01:26:00 GMT  
		Size: 164.2 KB (164194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3530a6477e7d4f65e20d0fc3159b1952d5a5cd03a0495670cb98b1c256672c9b`  
		Last Modified: Tue, 17 Mar 2026 01:26:01 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb40e2f14a7f835630b92bd0b542d418d0cbbd28342b2e76d9bdb5f959128a12`  
		Last Modified: Tue, 17 Mar 2026 01:26:01 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.12` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:01dc0050af908a88826e481a6fe45ad8e8782bc002e7b5d9ec3cec53e38e7a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4803799186b899adcabcfdea0581683d36340fb87f1fa54fad2c564575ee89`

```dockerfile
```

-	Layers:
	-	`sha256:8f01aec9bc34d0c3236f402502ed7516fb6aec320be30ac9044c2fe6eed392ab`  
		Last Modified: Tue, 17 Mar 2026 01:25:59 GMT  
		Size: 3.2 MB (3208984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5aa7cacccd159dddef6082f7390d28479e50577a32e8ba0101564e4d1e5930`  
		Last Modified: Tue, 17 Mar 2026 01:25:59 GMT  
		Size: 36.8 KB (36847 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.12` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:0d7fea19bed09ca9ab30e7e3d38fda09035bcbe7721e0fe4283cf791f41650d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564129883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad078579dd0453cf78e7c3135dc059a3ee2ac6fdf40c060d82d8b77a5af3200`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:25:18 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 17 Mar 2026 01:25:18 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 17 Mar 2026 01:25:18 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Mar 2026 01:25:18 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 17 Mar 2026 01:26:21 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 17 Mar 2026 01:26:21 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Mar 2026 01:26:21 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:26:21 GMT
ENV SHELL=/bin/bash
# Tue, 17 Mar 2026 01:26:21 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:26:21 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 17 Mar 2026 01:26:21 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Mar 2026 01:26:22 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Mar 2026 01:26:22 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 17 Mar 2026 01:26:22 GMT
LABEL org.label-schema.build-date=2026-02-23T23:08:40.713020893Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=840cd2a58b052d1632219ee0b8dcc0f364226287 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.12 org.opencontainers.image.created=2026-02-23T23:08:40.713020893Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=840cd2a58b052d1632219ee0b8dcc0f364226287 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.12
# Tue, 17 Mar 2026 01:26:22 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:26:22 GMT
CMD ["eswrapper"]
# Tue, 17 Mar 2026 01:26:22 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae2b5b22d25e026f5cb2dd868ee271227a33dcffa1c8645cdf94542329ef131`  
		Last Modified: Tue, 17 Mar 2026 01:27:01 GMT  
		Size: 6.0 MB (6039218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb1742ebdd86d19796299717941feff514b80596750af869570f396c8487a28`  
		Last Modified: Tue, 17 Mar 2026 01:27:01 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bad19e4bfc0f4da1bb9ba6c78d82e3d348308c165e258475d7f9e6a13ad9fb2`  
		Last Modified: Tue, 17 Mar 2026 01:27:12 GMT  
		Size: 528.9 MB (528929933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fa28997745d13bf4be6548697c220c831c098e54d57b0c0cbca298e6c480e4`  
		Last Modified: Tue, 17 Mar 2026 01:27:01 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3215fbdbd35ebbefe1b46f7fc895b1a96bfb6cae4ac00ee156a45d920dbc0042`  
		Last Modified: Tue, 17 Mar 2026 01:27:02 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b257e7ff2f8d70918c9d3f87d4cb032d3920dfe9fc8d86fa4f534f01884db7fb`  
		Last Modified: Tue, 17 Mar 2026 01:27:02 GMT  
		Size: 160.7 KB (160700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4378862ae2463ddbe5aa837c7583db566b4c9835bd5872b80570ae7487c3b059`  
		Last Modified: Tue, 17 Mar 2026 01:27:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4129a16007c500dd2668314f81ce6398ded76970c8f1211422421c1c212d6edf`  
		Last Modified: Tue, 17 Mar 2026 01:27:03 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.12` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8f5383bef57cebdf3199685b8d13bdae7e28aa0f6eda3c31c9732e8787c81068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf3f2ae2c35657d197392c83e571f8242e8cb02e81826458ec063a1ea8bd8e2`

```dockerfile
```

-	Layers:
	-	`sha256:24682e3e854ac56c8aa98123d27a4e46b0373559b7a07d1971aec75443efd029`  
		Last Modified: Tue, 17 Mar 2026 01:27:01 GMT  
		Size: 3.2 MB (3209397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe9ca7e56b8be16fd48304fbc0f5e2b97c367657d93c83378a52a9b4162796b`  
		Last Modified: Tue, 17 Mar 2026 01:27:00 GMT  
		Size: 37.0 KB (37048 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.6`

```console
$ docker pull elasticsearch@sha256:7ba54d964be63bd33510243f6fae9c162348b281bea49a917ab7458076ac4105
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:79b9736e85ba69dd2635c32e77fcaa3820620d9fd916ec3100200fbe4f89c98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.4 MB (738420542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2fdb5a7b96e60bb179100c5d5654f13072f76288b513516fcce91e678c6d2d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:51:30 GMT
ENV container oci
# Wed, 11 Mar 2026 04:51:31 GMT
COPY dir:c1ba4c335e7831ddebf5732b67e3739a636a3d3dbf6b4d4089ed8f31a1bfbfd1 in /      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:51:31 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:32 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:51:18Z" "org.opencontainers.image.created"="2026-03-11T04:51:18Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:51:18Z
# Wed, 11 Mar 2026 18:37:14 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:37:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 11 Mar 2026 18:38:31 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:38:31 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 11 Mar 2026 18:38:31 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 11 Mar 2026 18:38:41 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 11 Mar 2026 18:38:41 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 11 Mar 2026 18:38:41 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:38:41 GMT
ENV SHELL=/bin/bash
# Wed, 11 Mar 2026 18:38:41 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:38:41 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 11 Mar 2026 18:38:41 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 11 Mar 2026 18:38:41 GMT
LABEL org.label-schema.build-date=2026-02-23T23:37:17.026418401Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b6e59ddaac5fc0c537d10132b2a1d5511ff8b1b5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-23T23:37:17.026418401Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b6e59ddaac5fc0c537d10132b2a1d5511ff8b1b5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6
# Wed, 11 Mar 2026 18:38:41 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.6 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 11 Mar 2026 18:38:41 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 11 Mar 2026 18:38:41 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 11 Mar 2026 18:38:41 GMT
CMD ["eswrapper"]
# Wed, 11 Mar 2026 18:38:41 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1174ed37633caad5219e59c67f05fe4e54bd728c7a8cfd4ea1df16de15de2f76`  
		Last Modified: Wed, 11 Mar 2026 06:07:51 GMT  
		Size: 40.0 MB (39990896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96e78857fbc3e30ec457144a7891054575ef47fb67c174d245991f0a4c63b2f`  
		Last Modified: Wed, 11 Mar 2026 18:39:34 GMT  
		Size: 4.3 MB (4281627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212645c50a90e838be90fc089c30262fc13d6ee76dce0c94db7e33d8fef5331`  
		Last Modified: Wed, 11 Mar 2026 18:39:33 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab79c65eb2dfa106200b414fd6c3e5e54ca62bcc5516243c8498ec120eaacca4`  
		Last Modified: Wed, 11 Mar 2026 18:39:34 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e764822bce5c20ff0c8ff12d23cd8f7d89a285a69ecd2ce487bf10adce6d78`  
		Last Modified: Wed, 11 Mar 2026 18:39:46 GMT  
		Size: 694.1 MB (694058065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc2e5ae90646bdcc3a5a437c5a8dee6a5ed841aec4696921d2d0e88591dbda`  
		Last Modified: Wed, 11 Mar 2026 18:39:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c048634f1827b7c182ae3f8729257078aebade68cfbce58702c94c58d0832e`  
		Last Modified: Wed, 11 Mar 2026 18:39:35 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a006a65fbed3b479c128dabebf33f82e4e580a3336012bd45e80becdc6afd9d`  
		Last Modified: Wed, 11 Mar 2026 18:39:35 GMT  
		Size: 75.2 KB (75183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6d51a63e86252decbeef0f0816857c24e4ac7ffb649af22909f0ff8aa360b9`  
		Last Modified: Wed, 11 Mar 2026 18:39:36 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6a32cedb5cb2f0b3f2dd0902b81f950fbc7790178d5ea8a3e17a38ccba29248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21b52b5fabba27c3f2a3566dfb3681532566d9aa7c89f92006ec522a5fe068a`

```dockerfile
```

-	Layers:
	-	`sha256:eef39681dbd01f9f91db378d32cee093b9acf0816ea3434f12d51b0db8907fee`  
		Last Modified: Wed, 11 Mar 2026 18:39:34 GMT  
		Size: 2.1 MB (2098149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886a9f83d19c8a6a1750b9226e72c4ea803267fda96dfd19140181bb48b1e9e6`  
		Last Modified: Wed, 11 Mar 2026 18:39:34 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:64514c4493650454b724416de57757de971b9e1949f323b59fa6d5d0fa1443bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.5 MB (582480225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5027abe4bc24ffcc66a30c5243a327c5d91b1cd02cc4fffda2e46ff161e260`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:19 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:20 GMT
COPY dir:7796b64b73526e8dad6fca20071cfe57334a57323fbbb1f9256c4ffffa8b27db in /      
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:20 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:07Z" "org.opencontainers.image.created"="2026-03-11T04:53:07Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:07Z
# Wed, 11 Mar 2026 18:35:05 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:35:06 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 11 Mar 2026 18:36:01 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:36:01 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 11 Mar 2026 18:36:01 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 11 Mar 2026 18:36:07 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 11 Mar 2026 18:36:07 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 11 Mar 2026 18:36:07 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:36:07 GMT
ENV SHELL=/bin/bash
# Wed, 11 Mar 2026 18:36:07 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:36:07 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 11 Mar 2026 18:36:07 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 11 Mar 2026 18:36:07 GMT
LABEL org.label-schema.build-date=2026-02-23T23:37:17.026418401Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b6e59ddaac5fc0c537d10132b2a1d5511ff8b1b5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-23T23:37:17.026418401Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b6e59ddaac5fc0c537d10132b2a1d5511ff8b1b5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6
# Wed, 11 Mar 2026 18:36:07 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.6 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 11 Mar 2026 18:36:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 11 Mar 2026 18:36:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 11 Mar 2026 18:36:08 GMT
CMD ["eswrapper"]
# Wed, 11 Mar 2026 18:36:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a929c158045efa38dcdfac5809dfda6e7c13c225e0aae109412941b4ed8f3880`  
		Last Modified: Wed, 11 Mar 2026 06:07:49 GMT  
		Size: 38.2 MB (38205467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9953713fdc91e534971591aaef1185d3c4a37333078671f0b6100c753f69b3`  
		Last Modified: Wed, 11 Mar 2026 18:36:47 GMT  
		Size: 4.3 MB (4291713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b045ec2bc034a7fcf780c76dcca6616c0b20fb0761d4a760eac43dd50d785f87`  
		Last Modified: Wed, 11 Mar 2026 18:36:47 GMT  
		Size: 1.5 KB (1536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a06c64373e8ff804521726ed62faac111d5bda7bef37f71e10555e1fb5aa3f`  
		Last Modified: Wed, 11 Mar 2026 18:36:47 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadc215340fe4b7636e0e0f14a675bf1ac4949ff3fdd4818f8b048c2d95deb19`  
		Last Modified: Wed, 11 Mar 2026 18:37:00 GMT  
		Size: 539.9 MB (539894581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e981529bc5db56016d45e84068618adf9a718d7bed40979e18296f6cf97bab`  
		Last Modified: Wed, 11 Mar 2026 18:36:48 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c49991dd910266ba5025b10fb04069c7f0579f8fb2422575651aec4ed4de0`  
		Last Modified: Wed, 11 Mar 2026 18:36:48 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dafe9a39de449c4a4a3154523176dda86c497b5c88162b0193706e493c4935f2`  
		Last Modified: Wed, 11 Mar 2026 18:36:49 GMT  
		Size: 74.1 KB (74109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839386880b82aab47b00a3a58752764a73dca9f69373296151a8a89d15ec089a`  
		Last Modified: Wed, 11 Mar 2026 18:36:49 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a7467a3028bbd42de42c7f2358454c3f78117041d1a73e8466322f01417cbd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ad165402464ee594c3c002e9a63c60fe8d475c5c1f7d638c650c0401759968`

```dockerfile
```

-	Layers:
	-	`sha256:a5f36e5d3b67b15703d337846562d21e3874acc6e74d1aeff8759ac0c02068f3`  
		Last Modified: Wed, 11 Mar 2026 18:36:47 GMT  
		Size: 2.1 MB (2098711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99878a72a1d01ae67214dce195632a0c0484ba682fe5794e04ce6d1821526c09`  
		Last Modified: Wed, 11 Mar 2026 18:36:47 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.1`

```console
$ docker pull elasticsearch@sha256:8e638b6b2844a1f5321827e7f2822d435e835bd4ab4db00b00064d126553b29c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d5559f64c04a576c35b6a9cf058d505df30e4563892750fd3a28080c74c06290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716595107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d53e0873b2133c9e5d5bb3d303780b83a5d5cc45fc405edebe4a2866f93627e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:51:30 GMT
ENV container oci
# Wed, 11 Mar 2026 04:51:31 GMT
COPY dir:c1ba4c335e7831ddebf5732b67e3739a636a3d3dbf6b4d4089ed8f31a1bfbfd1 in /      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:51:31 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:32 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:51:18Z" "org.opencontainers.image.created"="2026-03-11T04:51:18Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:51:18Z
# Wed, 11 Mar 2026 18:35:25 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:35:25 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 11 Mar 2026 18:36:34 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:36:34 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 11 Mar 2026 18:36:34 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 11 Mar 2026 18:36:43 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 11 Mar 2026 18:36:43 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 11 Mar 2026 18:36:43 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:36:43 GMT
ENV SHELL=/bin/bash
# Wed, 11 Mar 2026 18:36:43 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:36:44 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 11 Mar 2026 18:36:44 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 11 Mar 2026 18:36:44 GMT
LABEL org.label-schema.build-date=2026-02-23T23:37:38.684779921Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0dd66e52ba3aa076cf498264e46339dbb71f0269 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-23T23:37:38.684779921Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0dd66e52ba3aa076cf498264e46339dbb71f0269 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1
# Wed, 11 Mar 2026 18:36:44 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.1 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 11 Mar 2026 18:36:44 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 11 Mar 2026 18:36:44 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 11 Mar 2026 18:36:44 GMT
CMD ["eswrapper"]
# Wed, 11 Mar 2026 18:36:44 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1174ed37633caad5219e59c67f05fe4e54bd728c7a8cfd4ea1df16de15de2f76`  
		Last Modified: Wed, 11 Mar 2026 06:07:51 GMT  
		Size: 40.0 MB (39990896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b671088aa968e2ca23415e6f7d1f85921bea8bd28fb8ec65dd635bbc82d0f72`  
		Last Modified: Wed, 11 Mar 2026 18:37:37 GMT  
		Size: 4.3 MB (4281583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e0a9f4a113b9d7e2360e00220fe663acd2fea9d561908813a0e7592555c33b`  
		Last Modified: Wed, 11 Mar 2026 18:37:37 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88530452794eabff67905eaf081501fc1818c88cc80f3bb0deb9883fe81429d1`  
		Last Modified: Wed, 11 Mar 2026 18:37:37 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b002502924236eceb3cc3e102c4c6a5646a1fe77b510b70d1472bd0c47199c`  
		Last Modified: Wed, 11 Mar 2026 18:37:51 GMT  
		Size: 672.2 MB (672232682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d00a65d7dbf05c5cd54c97346e383e93054fcca5d0cbe87a1429c572939b16`  
		Last Modified: Wed, 11 Mar 2026 18:37:38 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aa0b5d33678444069b28f3b0ec41fdeba7e876b9f89d6c25431a33113eaa67`  
		Last Modified: Wed, 11 Mar 2026 18:37:38 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc154ae848b9a9c383658e0de8ee4e5072206acfe8b21ce67732c64c03436027`  
		Last Modified: Wed, 11 Mar 2026 18:37:38 GMT  
		Size: 75.2 KB (75176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc1353ef74cb7673dabab3bd07faffe79086ee71271e2480ffda2f4dba44895`  
		Last Modified: Wed, 11 Mar 2026 18:37:39 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:54764ac84ab2183f651893c8d201888d8cc89c8aab7e4205a1a2c08bf67e9b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a33ad5013f96e13e70746fb000dd1649ca0711e585cf20a7bf29e9ed4075516`

```dockerfile
```

-	Layers:
	-	`sha256:a2fb5f132848b93b4ae8dbf77d8fd95ca0c8f99db3f11d2b23d73b769375d6fb`  
		Last Modified: Wed, 11 Mar 2026 18:37:37 GMT  
		Size: 2.1 MB (2089789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe9bc26f1e737d6499cdbe2eaf978f1f54018d78a1bcd6cd98ec412a6af7372`  
		Last Modified: Wed, 11 Mar 2026 18:37:37 GMT  
		Size: 33.9 KB (33855 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:2b6ab4095282cfba9c23bb55efdb4f9f269fedccb81931c20b3616c60c88648c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560633958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fa098aab13a9dac1c4d25c3c04303312b76acd8486da950c2daa8da249b326`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:19 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:20 GMT
COPY dir:7796b64b73526e8dad6fca20071cfe57334a57323fbbb1f9256c4ffffa8b27db in /      
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:20 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:07Z" "org.opencontainers.image.created"="2026-03-11T04:53:07Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:07Z
# Wed, 11 Mar 2026 18:34:49 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:34:49 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 11 Mar 2026 18:35:43 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:35:43 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 11 Mar 2026 18:35:43 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 11 Mar 2026 18:35:49 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 11 Mar 2026 18:35:49 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 11 Mar 2026 18:35:49 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:35:49 GMT
ENV SHELL=/bin/bash
# Wed, 11 Mar 2026 18:35:49 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:35:50 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 11 Mar 2026 18:35:50 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 11 Mar 2026 18:35:50 GMT
LABEL org.label-schema.build-date=2026-02-23T23:37:38.684779921Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0dd66e52ba3aa076cf498264e46339dbb71f0269 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-23T23:37:38.684779921Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0dd66e52ba3aa076cf498264e46339dbb71f0269 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1
# Wed, 11 Mar 2026 18:35:50 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.1 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 11 Mar 2026 18:35:50 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 11 Mar 2026 18:35:50 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 11 Mar 2026 18:35:50 GMT
CMD ["eswrapper"]
# Wed, 11 Mar 2026 18:35:50 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a929c158045efa38dcdfac5809dfda6e7c13c225e0aae109412941b4ed8f3880`  
		Last Modified: Wed, 11 Mar 2026 06:07:49 GMT  
		Size: 38.2 MB (38205467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c8e99cb6fcf06e8a640e1fa8fbe16996f608090dc6e1476ee3c466c4bf6fd`  
		Last Modified: Wed, 11 Mar 2026 18:36:28 GMT  
		Size: 4.3 MB (4291789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a19a7c9bbbe5cbb4a45ce9390cdf26a9592d0fa004b0758a100bab023fad7bd`  
		Last Modified: Wed, 11 Mar 2026 18:36:28 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0072a81f7ca9d86b774b4483a701a78ef9c1507858188008b24191a28bf4c6b`  
		Last Modified: Wed, 11 Mar 2026 18:36:28 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884ff63e442109a8257987e62c9db28992fe8a6e6f0a8ea5f23f644ecce10141`  
		Last Modified: Wed, 11 Mar 2026 18:36:39 GMT  
		Size: 518.0 MB (518048246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f968fa6e565c68f66a01c36874847a017373b5abac213dee2496775d64372`  
		Last Modified: Wed, 11 Mar 2026 18:36:29 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efb839cb8e6a50280ddd7eb99e81830de55de16faf55208595d35d9223bad73`  
		Last Modified: Wed, 11 Mar 2026 18:36:29 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f516cc76aba6ba040d457874237eccb291079d9785ce9a9065af5536feb5792c`  
		Last Modified: Wed, 11 Mar 2026 18:36:30 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75571b91100c8d183a6d75f17a9296ee8fe72b4aac118cdd7f365101886f08d4`  
		Last Modified: Wed, 11 Mar 2026 18:36:30 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2de9c78ee9d1f3d3e018682754a69002e568c2a1c011b4341650dbc1c6c3ce34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdde7c61b7e3b8a68ac092277dcc3a39be1dd1875a4da982660f059af729c88`

```dockerfile
```

-	Layers:
	-	`sha256:ddc41931c513f406644d8e615d425580501321dcd03df86207bacd855fef1ed1`  
		Last Modified: Wed, 11 Mar 2026 18:36:28 GMT  
		Size: 2.1 MB (2090351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c5b53d1b45fcc3606d858cd6a83b351d68a4237467ce5ab92d732edfcacccd`  
		Last Modified: Wed, 11 Mar 2026 18:36:28 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
