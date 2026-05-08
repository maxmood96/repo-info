<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.15`](#elasticsearch81915)
-	[`elasticsearch:9.3.4`](#elasticsearch934)
-	[`elasticsearch:9.4.0`](#elasticsearch940)

## `elasticsearch:8.19.15`

```console
$ docker pull elasticsearch@sha256:8ff844933190136cec601777d633453f4008cc126a652257d5f63cd8e92207ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.15` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f0133ed868820f60fb71131147b4a9c2a7f9ed1bf197737b478e117509134ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.1 MB (719090942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7771ade2bcec882be63ddeed272422660b3923d889e1dcabc290ab378434ec0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Fri, 01 May 2026 00:10:05 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Fri, 01 May 2026 00:10:05 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 01 May 2026 00:10:05 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:10:05 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 01 May 2026 00:11:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Fri, 01 May 2026 00:11:20 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 01 May 2026 00:11:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:11:20 GMT
ENV SHELL=/bin/bash
# Fri, 01 May 2026 00:11:20 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 01 May 2026 00:11:20 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 01 May 2026 00:11:20 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 01 May 2026 00:11:21 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 01 May 2026 00:11:21 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 01 May 2026 00:11:21 GMT
LABEL org.label-schema.build-date=2026-04-28T13:06:49.648073236Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d9256c374e649e04ff0fa2dafd43402d35a3fb3a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.15 org.opencontainers.image.created=2026-04-28T13:06:49.648073236Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d9256c374e649e04ff0fa2dafd43402d35a3fb3a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.15
# Fri, 01 May 2026 00:11:21 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:11:21 GMT
CMD ["eswrapper"]
# Fri, 01 May 2026 00:11:21 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d278e6bfeef6987bd8b800e8e0da44b3025c628d3cd20c568610cf12c8f830`  
		Last Modified: Fri, 01 May 2026 00:12:14 GMT  
		Size: 4.5 MB (4529933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66403c0e6c28bb83e21a20b07a35e27eb106cf96fc0f986702189a279da75186`  
		Last Modified: Fri, 01 May 2026 00:12:14 GMT  
		Size: 3.5 KB (3531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca380ffdc0f6d31c003b9f05141e23c1024af19dc3e22a7fc8636db66e9ff639`  
		Last Modified: Fri, 01 May 2026 00:12:32 GMT  
		Size: 684.5 MB (684533086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18398e123c8f30aeb8142cef735ca617c17193401a82992fe23e45ddbe20c50`  
		Last Modified: Fri, 01 May 2026 00:12:14 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4f082421d60e291746161c7c565844bfa070695287e7ad0562221bc54b1b62`  
		Last Modified: Fri, 01 May 2026 00:12:15 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9132b14c4b3a952e808e5419fdd89c492dd61d8846fef055ecc0b5678eef5`  
		Last Modified: Fri, 01 May 2026 00:12:16 GMT  
		Size: 164.2 KB (164194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed4f9b6d9435d185142fa3da46e5a342cb7df8cf2f248863ca121cc4ce7166e`  
		Last Modified: Fri, 01 May 2026 00:12:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8a3628f3068a878765f9ca4e7323a58f129b1e31ffcf5d4e8a825b3e11b39`  
		Last Modified: Fri, 01 May 2026 00:12:17 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.15` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4bdb052f90295cd514616a4fa9f160dc88d71d4f6bc213d22e20a795864ce6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3243248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d2a7fd786148a303f5ef49985f9099ad494def07e579edfa7438bce35265b6`

```dockerfile
```

-	Layers:
	-	`sha256:73d0b94e5b9cb0ac59bd0ad63c012e7ddf7848f2be1972a84e94b9c599d92266`  
		Last Modified: Fri, 01 May 2026 00:12:14 GMT  
		Size: 3.2 MB (3206432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a71f6c8575767d4ef5708ba63aef308933ac7edc52232e534360bd33eedf6915`  
		Last Modified: Fri, 01 May 2026 00:12:14 GMT  
		Size: 36.8 KB (36816 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.15` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:1ad837cd6646bf02f112efb457bea6563d1cff7a485fad6edc6a4b951596c02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.1 MB (567053857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467ad5959c362fa9916b3dc2a810d8e2637c8e6334df8bc95c6ef1a1579a0b22`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Fri, 01 May 2026 00:09:39 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Fri, 01 May 2026 00:09:39 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 01 May 2026 00:09:39 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:09:39 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 01 May 2026 00:10:27 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Fri, 01 May 2026 00:10:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 01 May 2026 00:10:27 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:10:27 GMT
ENV SHELL=/bin/bash
# Fri, 01 May 2026 00:10:27 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 01 May 2026 00:10:27 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 01 May 2026 00:10:27 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 01 May 2026 00:10:27 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 01 May 2026 00:10:27 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 01 May 2026 00:10:27 GMT
LABEL org.label-schema.build-date=2026-04-28T13:06:49.648073236Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d9256c374e649e04ff0fa2dafd43402d35a3fb3a org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.15 org.opencontainers.image.created=2026-04-28T13:06:49.648073236Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d9256c374e649e04ff0fa2dafd43402d35a3fb3a org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.15
# Fri, 01 May 2026 00:10:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:10:27 GMT
CMD ["eswrapper"]
# Fri, 01 May 2026 00:10:27 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e976e1142e8fca98f4b406ee6a88465aea00b40ba1651813a86d0db607985a`  
		Last Modified: Fri, 01 May 2026 00:11:07 GMT  
		Size: 4.5 MB (4534711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba106a160b4483f8c39ae79c26c0095332929bdc0d817b7485c0623e6a7881eb`  
		Last Modified: Fri, 01 May 2026 00:11:07 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cb9bfc8db246da5680ab02d8ad523498b6666299b79233c5871ef6390ed739`  
		Last Modified: Fri, 01 May 2026 00:11:23 GMT  
		Size: 533.4 MB (533352356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a55519bd36bf97d3b24307d6c1aa0ff610624f2da979214607f245ab81907b`  
		Last Modified: Fri, 01 May 2026 00:11:07 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0b8aaeb1df212bfee5ddea4a7b7f0416c461b7aa91fdc2aa71cf19dedf1bdf`  
		Last Modified: Fri, 01 May 2026 00:11:09 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26a1914a92e6a41cc6449a4ad46ca3c4848e8e273aec4f739733c87356238d9`  
		Last Modified: Fri, 01 May 2026 00:11:09 GMT  
		Size: 160.7 KB (160690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c0e5da3a44561d14c72d95c0983b590fdd16e70264267a0b02e6b2257f4ff6`  
		Last Modified: Fri, 01 May 2026 00:11:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0155466af3b240c6383b78bd56050eb5bd98dfceb63b6302f7f6ef9c5ccbec36`  
		Last Modified: Fri, 01 May 2026 00:11:10 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.15` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:633dabe8395c44b41cded608baf1511c9ba368ec8a9223ab2afff22da82336af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3243864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cecf43f23851659b45fcff5e00f77d38656d700a7b79fbc70df7c2da4ddaeab`

```dockerfile
```

-	Layers:
	-	`sha256:9bdb51339625aef4cfddc0155f8f42d02fbd3eaa352d2d19874631bb36431456`  
		Last Modified: Fri, 01 May 2026 00:11:07 GMT  
		Size: 3.2 MB (3206845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d5937a84d5b99d58ecd06ce52d0902c44abcb21c6590bd2440d80539773104`  
		Last Modified: Fri, 01 May 2026 00:11:07 GMT  
		Size: 37.0 KB (37019 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.4`

```console
$ docker pull elasticsearch@sha256:354a1e72b1d2890ccd956271368357df707ff15986a2c3e5f14c646aead53ac5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:bee4daf314a6959a45bdc40ebe8db471aba208e751eb7142db2fe06083d10677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.3 MB (720334786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec368392c2093fd0cbd13b59c7a64bf5e9652f7278e5dd01181406c504f24436`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:21:39 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 08 May 2026 16:21:39 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 08 May 2026 16:22:10 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:22:10 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 08 May 2026 16:22:10 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 08 May 2026 16:22:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 08 May 2026 16:22:20 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 08 May 2026 16:22:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:22:20 GMT
ENV SHELL=/bin/bash
# Fri, 08 May 2026 16:22:20 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 16:22:20 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 08 May 2026 16:22:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 08 May 2026 16:22:20 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Fri, 08 May 2026 16:22:20 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 08 May 2026 16:22:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 08 May 2026 16:22:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 08 May 2026 16:22:20 GMT
CMD ["eswrapper"]
# Fri, 08 May 2026 16:22:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32052bad88d5b6249092f85432b3ef7ae097ffa31ff051baa01ab7071121da1`  
		Last Modified: Fri, 08 May 2026 16:23:10 GMT  
		Size: 4.3 MB (4277412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11256c8b5256c07a9c30e059e37e830651e9c27b4ccc1d9db2628cd259137d2`  
		Last Modified: Fri, 08 May 2026 16:23:10 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b8d8061a74159fa5a6214e62546fb07991ac2b44f7216003899d69b938b110`  
		Last Modified: Fri, 08 May 2026 16:23:10 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac04948c7e3427769cdfbad10eace46e7861226db33f92617e1ed2c2da179f`  
		Last Modified: Fri, 08 May 2026 16:23:24 GMT  
		Size: 676.0 MB (675972641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792009702c35b7f999a03f66ad3fa54f9a4e994855473b420ceab52c9c33399`  
		Last Modified: Fri, 08 May 2026 16:23:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425ee0f3f80894e628870dd6a7d48a440c505498295eac7d79067955cea2f2cd`  
		Last Modified: Fri, 08 May 2026 16:23:12 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a33037fa62d721b2a7df35f874c905fbfa0f7d81167efe31d5161be58e1678`  
		Last Modified: Fri, 08 May 2026 16:23:12 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023469aaf4e067d316cc13b99b276d15ca451482d9213dfcbaebe53ab07ac13a`  
		Last Modified: Fri, 08 May 2026 16:23:13 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f8bd0c892b8560cabdcd945c8c1d5a181f3d2a9393a5c43d1b1925ff1e41d25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b84b1060afc28ba198a5e9439a4943dcf54983ea76e3bac6fa84d8ef26c198b`

```dockerfile
```

-	Layers:
	-	`sha256:0614b7a9f55dd4ff344fd49f258469a60c758d9f8dbf6f912e459b4fb0678147`  
		Last Modified: Fri, 08 May 2026 16:23:11 GMT  
		Size: 2.1 MB (2087261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924c89271f2babfe873f43391919ef5c877e1032ce73a21b3a816165e8690b57`  
		Last Modified: Fri, 08 May 2026 16:23:10 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c4e68c2a5fc7cdb96d42a1e9573cde9cf4c1cd9ea2a7635f39a43e65c6b039bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564443254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749b5e8821c45538b1e460999e12b28e699ee260c64fa61f71b40a19417ff2dd`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 06 May 2026 12:57:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:57:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:57:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:57:02 GMT
ENV container oci
# Wed, 06 May 2026 12:57:03 GMT
COPY dir:658522d0a080af3309d9cd140f39d4866e8d82f0dbb45a592dba1356f2d8aac5 in /      
# Wed, 06 May 2026 12:57:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:57:03 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:50Z" "org.opencontainers.image.created"="2026-05-06T12:56:50Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:50Z
# Fri, 08 May 2026 16:21:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 08 May 2026 16:21:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 08 May 2026 16:22:15 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:22:15 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 08 May 2026 16:22:15 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 08 May 2026 16:22:21 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 08 May 2026 16:22:21 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 08 May 2026 16:22:21 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:22:21 GMT
ENV SHELL=/bin/bash
# Fri, 08 May 2026 16:22:21 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 16:22:22 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 08 May 2026 16:22:22 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 08 May 2026 16:22:22 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Fri, 08 May 2026 16:22:22 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 08 May 2026 16:22:22 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 08 May 2026 16:22:22 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 08 May 2026 16:22:22 GMT
CMD ["eswrapper"]
# Fri, 08 May 2026 16:22:22 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4432ba7926545d58c5c1a534c052b34ad23c14c54c95de1caf5071ea5ef8f194`  
		Last Modified: Wed, 06 May 2026 13:31:32 GMT  
		Size: 38.2 MB (38205674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ed84895ea5867d33e34fb50212fdf66c7de668c2d5a059629aeb19caaf7fa3`  
		Last Modified: Fri, 08 May 2026 16:23:01 GMT  
		Size: 4.3 MB (4283864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d48df543361179da41b00d7ab749622d83c818823da1fe69f18791e7def706`  
		Last Modified: Fri, 08 May 2026 16:23:01 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c6ff8482623faa620493c30a4db5de443acb52b61cb5ffcf8c04bb4102f158`  
		Last Modified: Fri, 08 May 2026 16:23:01 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fe725d87a18af2d80214ba609485445e122746ffc1a34aa6bca51dc99a03f6`  
		Last Modified: Fri, 08 May 2026 16:23:11 GMT  
		Size: 521.9 MB (521865268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab40c2a1235c76741d392fe882aee6bcc1e34b2aba65210ac9b8a728581ec45`  
		Last Modified: Fri, 08 May 2026 16:23:02 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da9551b6d07b89f360cecf48fccc53849cf0b132849221fb8b0a268931090ae`  
		Last Modified: Fri, 08 May 2026 16:23:02 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2060b452dc0dd386f719e0cc4f207e08fd6a3d761658000f5f5cd432ebba6aaf`  
		Last Modified: Fri, 08 May 2026 16:23:03 GMT  
		Size: 74.1 KB (74103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95663afd0be6b2a01224b1e137d9cece2220404220546211c754f122c81c2917`  
		Last Modified: Fri, 08 May 2026 16:23:04 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3bfb0622ca353d054014baf5584bd8cd2033fc80d2619c0f43fdfced7d11556e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1259ea3357bc511c54f3a36463740442a91f88632b1ab8dd84b7b21c0f5026`

```dockerfile
```

-	Layers:
	-	`sha256:072e8d94599b14520bdf9836df5ac0bd40a339a21280350752c1f1adb5a5213e`  
		Last Modified: Fri, 08 May 2026 16:23:01 GMT  
		Size: 2.1 MB (2087823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae6365320fd1f7b291b9ce48625570072110d147bf7fc5712a65183467bcea4`  
		Last Modified: Fri, 08 May 2026 16:23:01 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.0`

```console
$ docker pull elasticsearch@sha256:814d6ffd6a71ed580df2c7d5a62354bbd627146f992b8042fc9bffe46b259a82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:7b525789ea24eab6126ff134032df4665b9613865143c44f50a410b388a0a765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.1 MB (864097267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8737d43b6320cbb771a042a4479c868a1944f8c6dcf04b91b46bfc816271e9`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:21:46 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 08 May 2026 16:21:46 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 08 May 2026 16:22:16 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:22:16 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 08 May 2026 16:22:16 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 08 May 2026 16:22:27 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 08 May 2026 16:22:28 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 08 May 2026 16:22:28 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:22:28 GMT
ENV SHELL=/bin/bash
# Fri, 08 May 2026 16:22:28 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 16:22:28 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 08 May 2026 16:22:28 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 08 May 2026 16:22:28 GMT
LABEL org.label-schema.build-date=2026-04-30T15:05:34.751113474Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2e8528e92361c3399724226deaf2b46f933e925b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T15:05:34.751113474Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2e8528e92361c3399724226deaf2b46f933e925b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Fri, 08 May 2026 16:22:28 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 08 May 2026 16:22:28 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 08 May 2026 16:22:28 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 08 May 2026 16:22:28 GMT
CMD ["eswrapper"]
# Fri, 08 May 2026 16:22:28 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4779cec36adae723f2e9830666482186da2d0d20f5435ca1044fc662f9fc7d`  
		Last Modified: Fri, 08 May 2026 16:23:27 GMT  
		Size: 4.3 MB (4277426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbe788b930c891adead648eea9f05f27da1347858ad6c0524b4e9c6e23b18e1`  
		Last Modified: Fri, 08 May 2026 16:23:26 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a59c899faef272fcc8057a18fba3d9567c0c6707ec595ca767d066095cebbf`  
		Last Modified: Fri, 08 May 2026 16:23:26 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0693ca6d01981fab689cc0797ab71701dd0b6bc0803d72a0b7598c024f5cef11`  
		Last Modified: Fri, 08 May 2026 16:23:41 GMT  
		Size: 819.7 MB (819735103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ec14c2ad009613060eb1892dbca00803693de2dca31a582c8acde3d3dc1c4`  
		Last Modified: Fri, 08 May 2026 16:23:27 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92069b3575b73084e4f0c2a96e6b495c9be0ccc6e55b48e10eb63a472a0eedcd`  
		Last Modified: Fri, 08 May 2026 16:23:28 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70deb0ec40cbe8ff8a2897625faecd9e53fc0a67ed4c9ef96c55bbaa95c8fbe`  
		Last Modified: Fri, 08 May 2026 16:23:28 GMT  
		Size: 75.2 KB (75183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbdf86e338c31a394c481fbde2f9733e47f49bbbf9a20edd2fd646d5120fac2`  
		Last Modified: Fri, 08 May 2026 16:23:29 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3b90e3f6f774231a5ac982cebbf62bc4d90c22294c6b283565e79a8e768d46a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:face7bfa334ab38c48ea68a6538284523e88a95a674515319d4a4dd8d83a7661`

```dockerfile
```

-	Layers:
	-	`sha256:383a49ce48050d3e7f4e8b546d66efb689521d425a3d2f5e42e020347f7f8a0d`  
		Last Modified: Fri, 08 May 2026 16:23:27 GMT  
		Size: 2.4 MB (2389450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1968e94559824563c00dc858e4d980f0382acdd8c8cd836d31f12da2a3bf3934`  
		Last Modified: Fri, 08 May 2026 16:23:26 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:735114ec4c1ab46c7638a44fe5802a4c3e7daf674bfff237dc9afb64a259366d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.8 MB (708773296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7ace9762b16444c1570f1d3dba596c3fcc97ac0cdbcc94a2d0c7dad808480`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 06 May 2026 12:57:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:57:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:57:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:57:02 GMT
ENV container oci
# Wed, 06 May 2026 12:57:03 GMT
COPY dir:658522d0a080af3309d9cd140f39d4866e8d82f0dbb45a592dba1356f2d8aac5 in /      
# Wed, 06 May 2026 12:57:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:57:03 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:50Z" "org.opencontainers.image.created"="2026-05-06T12:56:50Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:50Z
# Fri, 08 May 2026 16:21:24 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 08 May 2026 16:21:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 08 May 2026 16:22:29 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:22:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 08 May 2026 16:22:29 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 08 May 2026 16:22:37 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 08 May 2026 16:22:37 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 08 May 2026 16:22:37 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:22:37 GMT
ENV SHELL=/bin/bash
# Fri, 08 May 2026 16:22:37 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 08 May 2026 16:22:37 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 08 May 2026 16:22:37 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 08 May 2026 16:22:37 GMT
LABEL org.label-schema.build-date=2026-04-30T15:05:34.751113474Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2e8528e92361c3399724226deaf2b46f933e925b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T15:05:34.751113474Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2e8528e92361c3399724226deaf2b46f933e925b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Fri, 08 May 2026 16:22:37 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 08 May 2026 16:22:37 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 08 May 2026 16:22:37 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 08 May 2026 16:22:37 GMT
CMD ["eswrapper"]
# Fri, 08 May 2026 16:22:37 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4432ba7926545d58c5c1a534c052b34ad23c14c54c95de1caf5071ea5ef8f194`  
		Last Modified: Wed, 06 May 2026 13:31:32 GMT  
		Size: 38.2 MB (38205674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a8cfe1456bfac231bd99a901a9c05583f6b9c1c7fbd3a452eae32764a70b51`  
		Last Modified: Fri, 08 May 2026 16:23:24 GMT  
		Size: 4.3 MB (4283886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45fe9d31d7cda82fe06204542f90cda13c221498d8f1db0e7775e2a1a9e3565`  
		Last Modified: Fri, 08 May 2026 16:23:24 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8001f2157ce6ddcd96779f3593eaaf3900af393c44851aed60a18b42b812968`  
		Last Modified: Fri, 08 May 2026 16:23:24 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff06cc62d2ae35fa0899302b75dc20923c19dece30626bd2bc12a6adffd6e6b0`  
		Last Modified: Fri, 08 May 2026 16:24:01 GMT  
		Size: 666.2 MB (666195277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14914346f395f0929da5d48148e88588b3398424307c8723974669469fd4b10`  
		Last Modified: Fri, 08 May 2026 16:23:25 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138ee0783f83f4465cac4581704c7d4ee7ef8b823325160532c4da37c2184dfc`  
		Last Modified: Fri, 08 May 2026 16:23:25 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbcefcaf72aae9c4c55e0059234b54100fa711fdd3f9416378fce5189e1f53b`  
		Last Modified: Fri, 08 May 2026 16:23:26 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fd666fa7510c5624e31f38373eedef0c7acdca93cdc607233c154af3769fa`  
		Last Modified: Fri, 08 May 2026 16:23:27 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4b38dd9ce54f2989874ca515ce7f426e435dc133f93923d3136375619bc80f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6142dd542bfadb58fecf6855b219f524252a9d1888e3a2ac080eb10cf62e08`

```dockerfile
```

-	Layers:
	-	`sha256:653d6f849a55584e8b3844c739605a977fe3b25ef593d178259e409c8720b187`  
		Last Modified: Fri, 08 May 2026 16:23:24 GMT  
		Size: 2.4 MB (2390012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d862ea0316bf0809e8902bd7dd17ff09c842d816acc61991b9f45084805a37f6`  
		Last Modified: Fri, 08 May 2026 16:23:24 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json
