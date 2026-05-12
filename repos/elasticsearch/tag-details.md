<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.15`](#elasticsearch81915)
-	[`elasticsearch:9.3.4`](#elasticsearch934)
-	[`elasticsearch:9.4.1`](#elasticsearch941)

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
$ docker pull elasticsearch@sha256:5897ac98d723de52b1c13a87315887d90060724e69f524682252d628ceddb5e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9b388a2a9d7a106b512ed6091d3de38264fe62b7fa5cbde21813e624e207d1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.3 MB (720334754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe804c68038aa6cd7f08c61e9ed4a1059f0db03f37f3f47fe9511c2b2471145`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 11 May 2026 01:07:55 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:07:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:07:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:07:55 GMT
ENV container oci
# Mon, 11 May 2026 01:07:56 GMT
COPY dir:d396e6c334ec17a1ba4a03f21481f526666f77d114978313ef1df55edd8e1412 in /      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:07:56 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:07:39Z" "org.opencontainers.image.created"="2026-05-11T01:07:39Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:07:39Z
# Tue, 12 May 2026 00:07:13 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 May 2026 00:07:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 May 2026 00:07:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 00:07:48 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 00:07:48 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 May 2026 00:07:58 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 May 2026 00:07:58 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 May 2026 00:07:58 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:07:58 GMT
ENV SHELL=/bin/bash
# Tue, 12 May 2026 00:07:58 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 May 2026 00:07:58 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 May 2026 00:07:58 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 May 2026 00:07:58 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 12 May 2026 00:07:58 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 May 2026 00:07:58 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 00:07:58 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 May 2026 00:07:58 GMT
CMD ["eswrapper"]
# Tue, 12 May 2026 00:07:58 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:34f4a557df8123a31168a9ed57304a4ee0a79b26712d1770dcf7c798372b100b`  
		Last Modified: Mon, 11 May 2026 02:10:30 GMT  
		Size: 40.0 MB (39994724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a303218fe4be7824fd0864dbb96cd8f324c68985e31f1f34b9c3fc87e9f493f6`  
		Last Modified: Tue, 12 May 2026 00:08:51 GMT  
		Size: 4.3 MB (4277494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cd09c04f2afdfb61c410ccdb972df08fb020f80ab2810df58a56c553de9962`  
		Last Modified: Tue, 12 May 2026 00:08:50 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce8d75d20fc91e3dff87f0f3bd3c6cb77dbc38a612d73646bb88f7fbb047462`  
		Last Modified: Tue, 12 May 2026 00:08:50 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bbf5856b58606ae000b331fd4bcc7380cc9cb1aad643a74007bb39ca5fd11f`  
		Last Modified: Tue, 12 May 2026 00:09:06 GMT  
		Size: 676.0 MB (675972582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8fe9847e06b9a0e5256977fdf31e951c337d7bc5eb80ebd54f09fb8a985e32`  
		Last Modified: Tue, 12 May 2026 00:08:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae23a3cc3e5814d258d4e68f649c7130aa5840041dfb5cd043ce6567e67a0531`  
		Last Modified: Tue, 12 May 2026 00:08:51 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c97c2239876a4ddfe137f9de0eb0166c61f5b7d5b11cc4bad44ab58bafdf2a7`  
		Last Modified: Tue, 12 May 2026 00:08:52 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232c0a529fa55a1dfd0e35c8d0fa40f32dea0ff5b1979fa198f22e9e2542494b`  
		Last Modified: Tue, 12 May 2026 00:08:53 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:56c757a6fcf3af06d1bc1f9cc81bd99fce40fdf204513305e04459a51f8c3378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d080f7f60223ed05ffa9ea13dcb3c959b79aab3c87ed98d53972214b11cb423`

```dockerfile
```

-	Layers:
	-	`sha256:123b6aadac86117502888a01e8a604ee76dc582a2fdadbaf7e14c031c0b7a14b`  
		Last Modified: Tue, 12 May 2026 00:08:50 GMT  
		Size: 2.1 MB (2087263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d52b4df649f8f0137c5c3c149202d036d8f561df95f7c74245568a2f6ea54201`  
		Last Modified: Tue, 12 May 2026 00:08:50 GMT  
		Size: 33.9 KB (33855 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:af4539043255d779ac02a160b17fca40a06837a59c9fb0c2203da61a98cf1540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564443525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d633b529e5144853ada6ba158ff91c0e4a68128a4bcda57bee5ab98e977ea972`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 11 May 2026 01:10:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:10:04 GMT
ENV container oci
# Mon, 11 May 2026 01:10:05 GMT
COPY dir:f96b78a7f24437106ae6a323adf2c06c98f78157637998e58adf24d336fc59f9 in /      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:05 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:09:50Z" "org.opencontainers.image.created"="2026-05-11T01:09:50Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:09:50Z
# Tue, 12 May 2026 00:05:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 May 2026 00:05:15 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 May 2026 00:06:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 00:06:09 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 00:06:09 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 May 2026 00:06:15 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 May 2026 00:06:16 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 May 2026 00:06:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:06:16 GMT
ENV SHELL=/bin/bash
# Tue, 12 May 2026 00:06:16 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 May 2026 00:06:16 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 May 2026 00:06:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 May 2026 00:06:16 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 12 May 2026 00:06:16 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 May 2026 00:06:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 00:06:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 May 2026 00:06:16 GMT
CMD ["eswrapper"]
# Tue, 12 May 2026 00:06:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:07b48350f3398d184075c56877eb97837294903946c9a6c10031807b6c4f549d`  
		Last Modified: Mon, 11 May 2026 02:11:01 GMT  
		Size: 38.2 MB (38205518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9404cd80fb1f014a4f86db1bf7f40af488e80f2cc5507f351c737c742342852`  
		Last Modified: Tue, 12 May 2026 00:06:54 GMT  
		Size: 4.3 MB (4284348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a93fdb299f04c87360a3ce8108f2bf7eabb544d2f002ebb519f3010fbd170dd`  
		Last Modified: Tue, 12 May 2026 00:06:53 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97ba86dc410ae7dd31a4403a51b814533dbb42ac00e021cc350e5a5a7816d19`  
		Last Modified: Tue, 12 May 2026 00:06:53 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e30f327621a0791e950d996e3b9fc56425ef3e5462e41a64d5f00c7ffad60f5`  
		Last Modified: Tue, 12 May 2026 00:07:05 GMT  
		Size: 521.9 MB (521865212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80a77e14b0d3f8cf4bbcdfc81a3ad325188f9b9f929deb1e93c5830c16f248f`  
		Last Modified: Tue, 12 May 2026 00:06:55 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9452b70aa5880997d8717cb3a2fc677f75511deb519a489a3d035eb7303c9f51`  
		Last Modified: Tue, 12 May 2026 00:06:55 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b190a2ae44ceeae7693a39128bf3939082930309d584264114adc1b58a2c9586`  
		Last Modified: Tue, 12 May 2026 00:06:55 GMT  
		Size: 74.1 KB (74102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9567eb5051633a587ad9dd538feb690d138b115f53cd5e5178787addb6c91166`  
		Last Modified: Tue, 12 May 2026 00:06:56 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:fd3064fb5e1743743dfaf19ea5cb581a3343e74bcb3a2a593d7803db7ec2961d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddaeaea2518ab7c4c2e3022bd11c1805b52d1e79315a84154717d9ed5a0c101`

```dockerfile
```

-	Layers:
	-	`sha256:023e23e80aac303819cf4208ca46b559dc985e91b772f4c1f0d99eb9ffaaa376`  
		Last Modified: Tue, 12 May 2026 00:06:54 GMT  
		Size: 2.1 MB (2087825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f6de9a29c10ff503e29203d974521e69cf3f5ae5507eb1b41edb46bf85c42e3`  
		Last Modified: Tue, 12 May 2026 00:06:53 GMT  
		Size: 34.0 KB (34037 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.1`

**does not exist** (yet?)
