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
$ docker pull elasticsearch@sha256:a8894d718b629c435bbf6c91368b33c2f4c8122b2c4f402f620c39e16d004144
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9f003e7c2c4ea0d354b9b766cb256a475fc5a9728b642e76bdbd5ba7109ce24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.4 MB (720360719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e04f5ca4bbd3072e7011a07b35fc6acfe8a8ada09a31a02ab7c960361e8e3ab`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:09:03 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 05 May 2026 23:09:03 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 05 May 2026 23:09:27 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:09:27 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 05 May 2026 23:09:27 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 05 May 2026 23:09:37 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 05 May 2026 23:09:37 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 05 May 2026 23:09:37 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:37 GMT
ENV SHELL=/bin/bash
# Tue, 05 May 2026 23:09:37 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 May 2026 23:09:37 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 05 May 2026 23:09:37 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 05 May 2026 23:09:37 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 05 May 2026 23:09:37 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 05 May 2026 23:09:37 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 05 May 2026 23:09:37 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 05 May 2026 23:09:37 GMT
CMD ["eswrapper"]
# Tue, 05 May 2026 23:09:37 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03fb16d62a4a776b03bbfe5d0225a8da97dcff28bc5a803a16f3af3c6a6c513`  
		Last Modified: Tue, 05 May 2026 23:10:29 GMT  
		Size: 4.3 MB (4279039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d040ec58a1dbe75dabe32171c05afa62f3488fe6468aa22d6c857da3af65c0`  
		Last Modified: Tue, 05 May 2026 23:10:29 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73028b1ab141c534ea83edef6ca2932d289f5966c69547d96d3d5e43234b4576`  
		Last Modified: Tue, 05 May 2026 23:10:29 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34c7b82c13a563a8788d8ab4f5047df794a13d5e94941fa17e3f400012d4b9`  
		Last Modified: Tue, 05 May 2026 23:10:46 GMT  
		Size: 676.0 MB (675972619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c84b46a519467bf058c7b88e339bcbc6531c097a980a6b28a346fc0cf1f02bf`  
		Last Modified: Tue, 05 May 2026 23:10:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb7af182d2cfa4e37b0f8733a588dede3ce48a2c868bc856d77e29d6199720`  
		Last Modified: Tue, 05 May 2026 23:10:31 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0c8be90f2568538f767a6247f446ad590cd879fa6fbdbe15fe9dfada0ec5e`  
		Last Modified: Tue, 05 May 2026 23:10:31 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a26f7684e324ab25afc5a8c8a3bf89d13919c0ce90e9b609bbe2ef27401dad`  
		Last Modified: Tue, 05 May 2026 23:10:32 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f115055f65aaaac251ff67301e125d03fcf29002cf3e6dde20c1d827ccbf64d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c634e68267676691885ea64fe05fea8929b6c2b358490ab60aaec201dcb2218b`

```dockerfile
```

-	Layers:
	-	`sha256:9c5c77adf71d5bbf321773187355dcf85e3f8e23efcb30b9a9c9b4372463470b`  
		Last Modified: Tue, 05 May 2026 23:10:29 GMT  
		Size: 2.1 MB (2087261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7d703f9f237b3abe9028920f9e601be39bb545f9cd3988c5d197d92a81c0c5`  
		Last Modified: Tue, 05 May 2026 23:10:29 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:dc3925ea8c505dd6b0ea974bcf4ec9d8689da6382e38c09b49da210ce518adea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564443180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039af2bef9ff0c9af5672293279d880a4e8f19644d9bb3e9d5778cc45e6d106f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:08:48 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:48 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 05 May 2026 23:09:23 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:09:23 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 05 May 2026 23:09:23 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 05 May 2026 23:09:29 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 05 May 2026 23:09:29 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 05 May 2026 23:09:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:29 GMT
ENV SHELL=/bin/bash
# Tue, 05 May 2026 23:09:29 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 May 2026 23:09:29 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 05 May 2026 23:09:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 05 May 2026 23:09:29 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 05 May 2026 23:09:29 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 05 May 2026 23:09:29 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 05 May 2026 23:09:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 05 May 2026 23:09:29 GMT
CMD ["eswrapper"]
# Tue, 05 May 2026 23:09:29 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68291564852baf5521c89726962e5c7ea268eb46f5476f4b4e8229b3cbde99a`  
		Last Modified: Tue, 05 May 2026 23:10:08 GMT  
		Size: 4.3 MB (4283639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eda292ae4f6532798ae09811d000e091d88fa98fa35277a7a8d4d349db785e1`  
		Last Modified: Tue, 05 May 2026 23:10:08 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4824578bf362dc81dfccabc9033a0cf6f32665dc07c5a423eec293a4a0b8f5`  
		Last Modified: Tue, 05 May 2026 23:10:08 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03585eaee6810dac52819999542e972b1e6594881bfe7e6197391f70011f742a`  
		Last Modified: Tue, 05 May 2026 23:10:19 GMT  
		Size: 521.9 MB (521865270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65aad054bf0e4f194b317ca3592ba0c9c1747b88495e15205a960c6174f4d710`  
		Last Modified: Tue, 05 May 2026 23:10:09 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e663d542f81f998492f9a4a4054adb9c221ee25a9256e1e2e9946e5ab80622d`  
		Last Modified: Tue, 05 May 2026 23:10:09 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4671f0e5dacd68e13353530fe6ab7e6945f0cdac4b67e6789d564b2b65f28205`  
		Last Modified: Tue, 05 May 2026 23:10:10 GMT  
		Size: 74.1 KB (74103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f878124aa35e0794e178fc78ea2da9d9564d55c4bfb3df2588fada9c1658c`  
		Last Modified: Tue, 05 May 2026 23:10:10 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a4f269fcb0c0bca85b5da6381320330cae2f6125de422464f932b32d8b08372c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c2d30a9b8e0d6f049a9da00ab503a2fddd5cf9a4b2d2a8418f7e21a31675c9`

```dockerfile
```

-	Layers:
	-	`sha256:db07313193603bee2fc6a581a65195a4ab66279b154c94f243461869376b3507`  
		Last Modified: Tue, 05 May 2026 23:10:08 GMT  
		Size: 2.1 MB (2087823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744c873c75defce9c349c2dc8aee9554d2b422b4b5453a6e0ac372724aa19406`  
		Last Modified: Tue, 05 May 2026 23:10:08 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.0`

```console
$ docker pull elasticsearch@sha256:64e9e6284652bbb345f12e3fc0e967c4c731a5161f36474be75194ea80260bfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c0b0280c12bf0120be2456acf2a5a5ca46acedbcde292d574429085f14d5f63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.1 MB (864123213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c046b4f1aa725cda59004db750ea4d32076d735785886975ae4eb7d1c6a88835`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:09:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 05 May 2026 23:09:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 05 May 2026 23:09:45 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:09:45 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 05 May 2026 23:09:46 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 05 May 2026 23:09:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 05 May 2026 23:09:57 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 05 May 2026 23:09:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:57 GMT
ENV SHELL=/bin/bash
# Tue, 05 May 2026 23:09:57 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 May 2026 23:09:57 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 05 May 2026 23:09:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 05 May 2026 23:09:57 GMT
LABEL org.label-schema.build-date=2026-04-30T15:05:34.751113474Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2e8528e92361c3399724226deaf2b46f933e925b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T15:05:34.751113474Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2e8528e92361c3399724226deaf2b46f933e925b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Tue, 05 May 2026 23:09:57 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 05 May 2026 23:09:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 05 May 2026 23:09:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 05 May 2026 23:09:57 GMT
CMD ["eswrapper"]
# Tue, 05 May 2026 23:09:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7515e5377bff785732d40c104687396fab13aee8ee3c9ea2ab11f400a718959d`  
		Last Modified: Tue, 05 May 2026 23:10:51 GMT  
		Size: 4.3 MB (4279037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a4947945c65214ecf958d4144a367481039a18bdc9997d7415298303610791`  
		Last Modified: Tue, 05 May 2026 23:10:51 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17646acfdb3db2fd84cac233a098d85d939bd8720519a3efb2d3a65b8238803e`  
		Last Modified: Tue, 05 May 2026 23:10:51 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71a1b61da68eaba69896b6afa6fc3c72a5380a29de7308b3f596332e0e74c0d`  
		Last Modified: Tue, 05 May 2026 23:11:07 GMT  
		Size: 819.7 MB (819735105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02efa92d418d93103a41eacc331485d31fd671dd2d0ffbee052a3fd5ad14902d`  
		Last Modified: Tue, 05 May 2026 23:10:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20b86f5a2965332cfd6c32776df4506b09ed559a1e9453bab986d79e666d90a`  
		Last Modified: Tue, 05 May 2026 23:10:52 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49cf4bb8610cf0945b1da46d57d23e52abd7f02bbc88499435408608b3159fd`  
		Last Modified: Tue, 05 May 2026 23:10:52 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c6bae2b8107873fbe4d3bfc841503ddf80d87f3f1c9f3f8c8eaf8567f39f7c`  
		Last Modified: Tue, 05 May 2026 23:10:53 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2b45c5e6774e5613efdbd42ee1a81e1ba62bf0b4c293f0b8ef8a6b8d96044b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f14f6c4119067237723fff03db99168ca8589f66021b28ee1f3e30970d115`

```dockerfile
```

-	Layers:
	-	`sha256:386ff424649f8266330a6d3dd4f3eb3366ec436cf397583400f03e2c0033d7d3`  
		Last Modified: Tue, 05 May 2026 23:10:51 GMT  
		Size: 2.4 MB (2389450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7620796475338d64b9bd2b26b0f8a273416bd4aecce2df1256fa4e5d8b54407a`  
		Last Modified: Tue, 05 May 2026 23:10:50 GMT  
		Size: 33.8 KB (33775 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d6043f3248863effb308b2bac1cae3375235e76f6ffaab52c8f211943e5f0d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.8 MB (708773224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f46365818f8e4d6def8c5d9c61e41f3603c796be2b6bec055fa4e308c73458`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:08:55 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:55 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 05 May 2026 23:10:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:10:08 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 05 May 2026 23:10:08 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 05 May 2026 23:10:16 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 05 May 2026 23:10:16 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 05 May 2026 23:10:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:10:16 GMT
ENV SHELL=/bin/bash
# Tue, 05 May 2026 23:10:16 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 05 May 2026 23:10:16 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 05 May 2026 23:10:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 05 May 2026 23:10:16 GMT
LABEL org.label-schema.build-date=2026-04-30T15:05:34.751113474Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2e8528e92361c3399724226deaf2b46f933e925b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T15:05:34.751113474Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2e8528e92361c3399724226deaf2b46f933e925b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Tue, 05 May 2026 23:10:16 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 05 May 2026 23:10:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 05 May 2026 23:10:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 05 May 2026 23:10:16 GMT
CMD ["eswrapper"]
# Tue, 05 May 2026 23:10:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9624abb819516a6b00b289c5345ffbb47fb52a34c0db816895a3149c6dae784e`  
		Last Modified: Tue, 05 May 2026 23:11:02 GMT  
		Size: 4.3 MB (4283673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203c423d9b116a3654cef30a59f6c8904e510545760bb4f2afe2fd557b91de4e`  
		Last Modified: Tue, 05 May 2026 23:11:01 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c5b8fc5906304ff6d10a7e89672ce16ccb52cca55fcb7de4566905b4927a9`  
		Last Modified: Tue, 05 May 2026 23:11:01 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e5632121911d6e88e1c2fb7164d58782dc6f3302ba501ecffbc8782d1d8f1c`  
		Last Modified: Tue, 05 May 2026 23:11:23 GMT  
		Size: 666.2 MB (666195275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34544e01381550de8238010b1e27c913e866634a0e059955f11916e693a0fb1f`  
		Last Modified: Tue, 05 May 2026 23:11:02 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381cd33eab182b16c91396f515150c9d514c4c4b1fa955f603031c7601d1e5fc`  
		Last Modified: Tue, 05 May 2026 23:11:02 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed08dbe73fb8d0aebc9f0b839c2add9153231ad859d22fb2024a4c019403fd`  
		Last Modified: Tue, 05 May 2026 23:11:03 GMT  
		Size: 74.1 KB (74109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027eaf9c8d66b0998a84f641606c0f12e8496e70e6d524945a39b0cfdbed07bf`  
		Last Modified: Tue, 05 May 2026 23:11:04 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:338e8396546b9aeb6b2b71bf160722bad708ce0462a73bb05686505480b43597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43dab509d452ef0bd3c4e6aadad0a8bfc5a1af110c1f95a553e36d16c2b0f2`

```dockerfile
```

-	Layers:
	-	`sha256:0a898e3a6b587f2f649c734cb9dbd2f79c24b7f8cf147f0e5a317dcbe4267977`  
		Last Modified: Tue, 05 May 2026 23:11:02 GMT  
		Size: 2.4 MB (2390012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5c63e5313277a976b49337f58fc98cff8fe043c85401c375b786034e683408`  
		Last Modified: Tue, 05 May 2026 23:11:01 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json
