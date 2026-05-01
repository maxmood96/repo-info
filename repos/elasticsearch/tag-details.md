<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.15`](#elasticsearch81915)
-	[`elasticsearch:9.2.8`](#elasticsearch928)
-	[`elasticsearch:9.3.4`](#elasticsearch934)

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

## `elasticsearch:9.2.8`

```console
$ docker pull elasticsearch@sha256:6ac3b64568aab22e7808fbe9359185e95948279e88eb86a0e2b9f09989878cc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:53729edc09018d29765ade50d28fdad442c0c6f84c675c40a824000a944d1fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.5 MB (738508561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e55b444b1d528f8189ebf3988ef9944c684aacac6819073580c763242850e46`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Wed, 22 Apr 2026 18:17:42 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:42 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 22 Apr 2026 18:18:58 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:18:58 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:18:58 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 22 Apr 2026 18:19:08 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:19:08 GMT
ENV SHELL=/bin/bash
# Wed, 22 Apr 2026 18:19:08 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 22 Apr 2026 18:19:08 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 22 Apr 2026 18:19:08 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 22 Apr 2026 18:19:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 18:19:08 GMT
CMD ["eswrapper"]
# Wed, 22 Apr 2026 18:19:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db45f40a6c781d7d088e0937b126f90a2e87f8ab340a73485a620b3684b58d15`  
		Last Modified: Wed, 22 Apr 2026 18:20:01 GMT  
		Size: 4.3 MB (4276366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae84b2cf58330696eb95f861392a66ad91c31b39d928980c0c7a7a0cc9173d8`  
		Last Modified: Wed, 22 Apr 2026 18:19:56 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f405c87f1dcd707ec61a7875a6428714f1a47471eca00207ba6af7ddf31a5308`  
		Last Modified: Wed, 22 Apr 2026 18:20:00 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e897eee62fe7b9a805b8766312316a05f48d7145e5b5103f59a49be1eba30c`  
		Last Modified: Wed, 22 Apr 2026 18:20:15 GMT  
		Size: 694.1 MB (694117467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f02b9bf6eb9f64f7a4b9eee82053e45e2ed235ced04328dbc69bfbf81ae5dc`  
		Last Modified: Wed, 22 Apr 2026 18:20:00 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34318704563d3ae649d3715211bf00c2f5d27bf85e839d0d47845af289de1478`  
		Last Modified: Wed, 22 Apr 2026 18:20:02 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8dcfc0b7a0ddd892f4b91bc2af7443906efc676cfb7b04a189105b8eaa92f3`  
		Last Modified: Wed, 22 Apr 2026 18:20:02 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5356f53aaa2225e05855506f0a54a5b3225a01d43c760ec2a79c33440bfb`  
		Last Modified: Wed, 22 Apr 2026 18:20:02 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:960819260bb0d6e2db78c913e295dc2035f87ae9a9a6c0aab32acbfd3b801652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5df823bbc94f7d9240ae153491d3812076be7be18c4f01990cbbf0045e75bef`

```dockerfile
```

-	Layers:
	-	`sha256:8f4a7b393b3773119ca0377bc339ab37603c729fd25d088991b08ea9c722254a`  
		Last Modified: Wed, 22 Apr 2026 18:20:00 GMT  
		Size: 2.1 MB (2098165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c10a3d2dcbf0f5ea48b3d0c2ef7b794a4f4a267d756318e68fbea05983895ea`  
		Last Modified: Wed, 22 Apr 2026 18:20:00 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ada39bf6ffd4006f9ddafad13e78e7cb9011848230e9cc1c670e6bca4daa3ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.5 MB (582515655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557ae495c403b399e0ef48d25fd1da0c5078fc2c41cdc21c9c95b933f1a15eb8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Wed, 22 Apr 2026 18:17:09 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 22 Apr 2026 18:18:09 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:18:09 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:18:09 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 22 Apr 2026 18:18:16 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:18:16 GMT
ENV SHELL=/bin/bash
# Wed, 22 Apr 2026 18:18:16 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 22 Apr 2026 18:18:16 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 22 Apr 2026 18:18:16 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 22 Apr 2026 18:18:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 18:18:16 GMT
CMD ["eswrapper"]
# Wed, 22 Apr 2026 18:18:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e8788b95ae82b170d90d3a0f49acd8e344af859c7517019b20ec5b7cf41195`  
		Last Modified: Wed, 22 Apr 2026 18:18:57 GMT  
		Size: 4.3 MB (4284564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0e036a3b5ee68c7738d49c8ec2af4b3a68f8ca8f2bf8a47104913e1b46ca2c`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c89e860d32bef5a7824124ed114e512fc3352e503129dbf756abbdf52e54932`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70ec324e22df8de6cca5252ca593108057762fef2953fcd7ec6c2f8e97c6630`  
		Last Modified: Wed, 22 Apr 2026 18:19:12 GMT  
		Size: 539.9 MB (539938157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770d970e1768850a0940c0c932b81ab2cb612bf8936a1ba5ea9224f3f5c37c83`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812f28f382ced9d2f6ed7b9bdad94f34326bbc3f58f3423ed41960d59721e1ba`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb4b2dbfad009f6b3a2bd651aae714feb38be5a67b186cdc8316cbf400ff24f`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad421c221b52a8a76351974bb39a258335a0302894528da90eda46675cf526a`  
		Last Modified: Wed, 22 Apr 2026 18:18:59 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0caead6a4788a86e30d9c6f5280a2708048794894b377941719e0888b5e9a125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89df5df39b32ef67239636de4518427c9e06929d93d08c4dcdffa6309ada20e7`

```dockerfile
```

-	Layers:
	-	`sha256:a20d6493075a3a608e65017e43de86cbe3d4cea6d3b56fd94b99ce6c91037fea`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 2.1 MB (2098727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48ebab63fc320e3fcf2019e0fb09135886075f508788dc034ff859144061763`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.4`

```console
$ docker pull elasticsearch@sha256:5dd1ab8e73bf66668abcde5892b10c2fef39269b80639a5cd0d5b224207a2ba3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6c9c50319e27d457c721271b999d0db0a981c30bbbebb5b9a473e76983d95432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.4 MB (720363761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e07068594f3b4c4982cac90dd3dd7c539d39d587b0f1f9291edcf1ad7d8c33`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Fri, 01 May 2026 00:09:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 01 May 2026 00:09:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 01 May 2026 00:11:06 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:11:06 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 01 May 2026 00:11:06 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 01 May 2026 00:11:16 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 01 May 2026 00:11:16 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 01 May 2026 00:11:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:11:16 GMT
ENV SHELL=/bin/bash
# Fri, 01 May 2026 00:11:16 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 01 May 2026 00:11:16 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 01 May 2026 00:11:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 01 May 2026 00:11:16 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Fri, 01 May 2026 00:11:16 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 01 May 2026 00:11:17 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 01 May 2026 00:11:17 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:11:17 GMT
CMD ["eswrapper"]
# Fri, 01 May 2026 00:11:17 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da21f1aaca8db74c1d2a940b343671681698ff9fe1e65884395f049c2b951c16`  
		Last Modified: Fri, 01 May 2026 00:12:09 GMT  
		Size: 4.3 MB (4276381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ad2830e1eb283619dc846eb080c2c9922d1c0ca1f6cbfa473d795d00466920`  
		Last Modified: Fri, 01 May 2026 00:12:09 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099bca1d5e4baeb17992190ce174cd2e3f237f994687ea04b27126048c3ae088`  
		Last Modified: Fri, 01 May 2026 00:12:09 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c4c8689c962a5f1b8d8f8f8933874082d6e6c0d8f5df91b66df5e42b570816`  
		Last Modified: Fri, 01 May 2026 00:12:22 GMT  
		Size: 676.0 MB (675972649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97a04f5a2909bb7bf495a9dc811d7e9e1edf92b8d54cee9a22cd3e2d81af252`  
		Last Modified: Fri, 01 May 2026 00:12:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b876e811ef8c149d722af2a7ceb8b57dab8cf2d185eb81be0f551bbdf57455f`  
		Last Modified: Fri, 01 May 2026 00:12:10 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dd500a98eb72c84ae0038845e538c15145c8bf4097d8301373ac8eb7d94cae`  
		Last Modified: Fri, 01 May 2026 00:12:11 GMT  
		Size: 75.2 KB (75183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bbb70fced06f6ec434a05481ffd9f75cc876c8fcc013968682ea0ae0978d62`  
		Last Modified: Fri, 01 May 2026 00:12:11 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9fc168d8a47f2f5e30bbede80fd4914ae034460f5e1a546e834ec97993271a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46403866ae6334ccc49de823eb19b29285483d9b50ddcf19ad34ea7d281f29a6`

```dockerfile
```

-	Layers:
	-	`sha256:b7fa54e14b846b36cd94f7192e60dc06e0200bbed2bc4d56ab60238b55109e97`  
		Last Modified: Fri, 01 May 2026 00:12:09 GMT  
		Size: 2.1 MB (2087253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9855ad3506fccf8b866f49e4cf2f98f17fdbdca88205c4315bf9408267e6744b`  
		Last Modified: Fri, 01 May 2026 00:12:09 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:0f754cff93431f0ee7e1eeacd2e25e01dcd4e961aefd58b62a245f521acfe041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564442797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5bbf3d9cfa57b1afdd2f0bdee02576b9264adf4748a77283168b08ec229b5f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Fri, 01 May 2026 00:09:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 01 May 2026 00:09:26 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 01 May 2026 00:10:00 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:10:00 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 01 May 2026 00:10:00 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 01 May 2026 00:10:06 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 01 May 2026 00:10:06 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 01 May 2026 00:10:06 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:10:06 GMT
ENV SHELL=/bin/bash
# Fri, 01 May 2026 00:10:06 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 01 May 2026 00:10:06 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 01 May 2026 00:10:06 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 01 May 2026 00:10:06 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Fri, 01 May 2026 00:10:06 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 01 May 2026 00:10:06 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 01 May 2026 00:10:06 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 01 May 2026 00:10:06 GMT
CMD ["eswrapper"]
# Fri, 01 May 2026 00:10:06 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854f018124bdd83f7b13c070dad2e69946ca92e718ff6f36077462814688a92a`  
		Last Modified: Fri, 01 May 2026 00:10:44 GMT  
		Size: 4.3 MB (4284554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31db2cb2a7249a61c6981b1014a95e70fe72010b4b5d07d90b6c4d6a45bb66e4`  
		Last Modified: Fri, 01 May 2026 00:10:44 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af1da88095af21d93526216049a6d7d0c5dee6a40d6d52f0a4320a4ce031a1e`  
		Last Modified: Fri, 01 May 2026 00:10:44 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11932f7d332c9e8cb9f4b6e1c76434a52064f542d8547d93e76cf47f370e11e`  
		Last Modified: Fri, 01 May 2026 00:10:55 GMT  
		Size: 521.9 MB (521865296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aff99935bba95f695508b2721fb9f0d9474131586c467ab2e2e64f428b6ec4e`  
		Last Modified: Fri, 01 May 2026 00:10:45 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94930fbc26fcd588e5d664c480cf53df135a4f889bd7ea9f07921842dbfb4a3`  
		Last Modified: Fri, 01 May 2026 00:10:46 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21efe251dda5abf23a4b0bbff2ae99341cc7c1d48d43a92be33be671572cbd45`  
		Last Modified: Fri, 01 May 2026 00:10:46 GMT  
		Size: 74.1 KB (74107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8679720e78d16e8c2c79d63a64bda32af3acbc1cb8a2e96d5766bd781c5a7a`  
		Last Modified: Fri, 01 May 2026 00:10:47 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e0a961c5d8393eafa513c5ce6d670243b024d627f877864ae6203974efc4284f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5c0a227d1d34e3326ca6ca1baf1360d878939f9c05838edf754bb0045aeac1`

```dockerfile
```

-	Layers:
	-	`sha256:7f70e192fbb973fd8695c0e8b834633c99b8d0375433b9ea291645b7cfcd0774`  
		Last Modified: Fri, 01 May 2026 00:10:45 GMT  
		Size: 2.1 MB (2087815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ca50d3f2f3e0a1192f81545161aef7f91b9356a9f91619986a2ce94cf6cdff`  
		Last Modified: Fri, 01 May 2026 00:10:44 GMT  
		Size: 34.0 KB (34036 bytes)  
		MIME: application/vnd.in-toto+json
