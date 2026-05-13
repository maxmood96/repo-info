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
$ docker pull elasticsearch@sha256:068914b1dc851bce64f3197baf35830ede00aeb323893bd28258ecd500915dcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a2f34a3b217517a0c33c79e17c9ff9a3dc9634d903b209bbe753e6b2a92ec533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.4 MB (720363677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ddbeac711687de483b87aea4e98d5f4253d69ebf6b719478ac1f0fe8eee5a0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 May 2026 05:07:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:07:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:07:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:07:30 GMT
ENV container oci
# Tue, 12 May 2026 05:07:31 GMT
COPY dir:5370c41d6d8459b92eabd7b14d9158353a8d692cfb39a86c0ad6f0e8377d5a95 in /      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:07:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:07:12Z" "org.opencontainers.image.created"="2026-05-12T05:07:12Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:07:12Z
# Tue, 12 May 2026 23:34:27 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 May 2026 23:34:27 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 May 2026 23:35:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 23:35:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 23:35:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 May 2026 23:35:30 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 May 2026 23:35:30 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 May 2026 23:35:30 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:35:30 GMT
ENV SHELL=/bin/bash
# Tue, 12 May 2026 23:35:30 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 May 2026 23:35:30 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 May 2026 23:35:30 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 May 2026 23:35:30 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 12 May 2026 23:35:30 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 May 2026 23:35:30 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 23:35:30 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 May 2026 23:35:30 GMT
CMD ["eswrapper"]
# Tue, 12 May 2026 23:35:30 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c06b8ad3393fea673394e067fccddfc7ef6d8cee753eba4c4dcd5d67792bfd4b`  
		Last Modified: Tue, 12 May 2026 06:00:36 GMT  
		Size: 40.0 MB (40022633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767aba4b8f2739d0566f838ecc3e46efb6e22dcf56fcb03705f5a5696580cf35`  
		Last Modified: Tue, 12 May 2026 23:36:22 GMT  
		Size: 4.3 MB (4278454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29db2616d849e4c10ed1b132cf69bb8c59e1589f23705827356b5aaa84bd37`  
		Last Modified: Tue, 12 May 2026 23:36:22 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d3c6aada16683c6c04b041b451e31b61ab76aa0ed56d1f1a1cde7f56e057fc`  
		Last Modified: Tue, 12 May 2026 23:36:22 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4b66e36b0091a4f0b3f2113e16d70006151c8e2697f24bcd32637f5b2f8fd0`  
		Last Modified: Tue, 12 May 2026 23:36:38 GMT  
		Size: 676.0 MB (675972637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f32e2aa1a2d358c497228fafade2f277813c85052933dea39affb9d8acfa8f1`  
		Last Modified: Tue, 12 May 2026 23:36:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3b8658afe11f7002eabce6430365f23b8802bdf5645521e1823fc9c45eb65b`  
		Last Modified: Tue, 12 May 2026 23:36:23 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca46ffd529ca20110ffa62898097f2d0105e0d0edaf5c336bb58e6e4e97e689`  
		Last Modified: Tue, 12 May 2026 23:36:24 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d294eeaa4be10f326d6132d0bc7a2b9588861636eca3f41918f732966fbabc`  
		Last Modified: Tue, 12 May 2026 23:36:25 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:dc77f7c06331cd4e39c2f21c01ca9857282d20656a42720638e4d8573b4491ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1098cf441eac19b6e180d3c6b930e329de3cee8da62abe9f5c81cdd64a276c35`

```dockerfile
```

-	Layers:
	-	`sha256:0f12804b126a7ec7a79ef816ba3d831403e60938a58237b984b8fbe1ab11540c`  
		Last Modified: Tue, 12 May 2026 23:36:22 GMT  
		Size: 2.1 MB (2087263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ccf000df068e43d7321796dbbc256902f731ffacb0b0fe2d798041968431308`  
		Last Modified: Tue, 12 May 2026 23:36:22 GMT  
		Size: 33.9 KB (33853 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b4adb45371709d938e8ee6cc5a5a960e2ae2470ff736d61dc9f2429598178a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564441307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8001f78af36c3f916af1471c56d495f484784ca93062d21b2d06d00da586882`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 May 2026 05:08:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:08:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:08:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:08:30 GMT
ENV container oci
# Tue, 12 May 2026 05:08:31 GMT
COPY dir:1ccd99245be3a0b58a1846f076e5b2ceb5e84e683dd2697432c08ac554789d9d in /      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:08:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:08:17Z" "org.opencontainers.image.created"="2026-05-12T05:08:17Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:08:17Z
# Tue, 12 May 2026 23:34:01 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 May 2026 23:34:01 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 May 2026 23:34:52 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 23:34:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 23:34:52 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 May 2026 23:34:58 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 May 2026 23:34:58 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 May 2026 23:34:58 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:34:58 GMT
ENV SHELL=/bin/bash
# Tue, 12 May 2026 23:34:58 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 May 2026 23:34:58 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 May 2026 23:34:58 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 May 2026 23:34:58 GMT
LABEL org.label-schema.build-date=2026-04-22T22:10:58.242616321Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T22:10:58.242616321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=69a3e6c50ebb57a1fdbf3f235be9f11061ac7d86 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 12 May 2026 23:34:58 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 May 2026 23:34:58 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 23:34:58 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 May 2026 23:34:58 GMT
CMD ["eswrapper"]
# Tue, 12 May 2026 23:34:58 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cd21d11a73b4a3fb6683533da05d561785e6bdfe61eb163870493206db32b8fc`  
		Last Modified: Tue, 12 May 2026 06:10:38 GMT  
		Size: 38.2 MB (38205025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cb60989fa6afd491e429f7e43606e3f1d6f2df7ee00aa11c9bfc69b655a337`  
		Last Modified: Tue, 12 May 2026 23:35:37 GMT  
		Size: 4.3 MB (4282688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84698a04a77fedf341cb9f0614e5917750bceb363ccbbae67db2ff869093f3d2`  
		Last Modified: Tue, 12 May 2026 23:35:37 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302928402375b0723310a61b53a563101a721d81d4e4848ca2d48994afb3b26a`  
		Last Modified: Tue, 12 May 2026 23:35:37 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61bcd0a012a562792278d70801f2944f55ead0799835d6080ad7cb9e9e4b506`  
		Last Modified: Tue, 12 May 2026 23:35:48 GMT  
		Size: 521.9 MB (521865143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f89e681055e9af36df9f524b7fef290e4fa1dd335f1e986c8d43722be0d347e`  
		Last Modified: Tue, 12 May 2026 23:35:38 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac282b2623ec9a210dbf5a2f8a8791a5d221c1e0183b0ae18a92b9c2d45bbb87`  
		Last Modified: Tue, 12 May 2026 23:35:38 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4326ce5993ddd5675094f33dc32d95c379c9e1c5651af1b5e459a91aaf72b2`  
		Last Modified: Tue, 12 May 2026 23:35:38 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eee44fd237c410a0eb83e1bf52a450e35cc19021091bd430cd04ebbe4b65dd8`  
		Last Modified: Tue, 12 May 2026 23:35:39 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ceea01f0a01d517de4c6852ef9813c3113fef75d9658ad36637350075695618a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4654884a9741d2f4912db889d48aadc427dceaf4bf6bf7b9f7fd29fcfcfcdb31`

```dockerfile
```

-	Layers:
	-	`sha256:69b41ca155f72caab85576c3da2bfcaef0065e99f621ab4ffa37ee2d5db4e750`  
		Last Modified: Tue, 12 May 2026 23:35:37 GMT  
		Size: 2.1 MB (2087825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899d043ff29e20bf8d513d1759b0c258df0b07df6fd9a41b6e6cbb051b29b8f7`  
		Last Modified: Tue, 12 May 2026 23:35:37 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.4.1`

```console
$ docker pull elasticsearch@sha256:12aec8d2b01e0447c61303fc04a66dfbb7bfbb6a1332faf32707c3a2b54787d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.4.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:dc0bab5391dbe8b02f886c6458c74892cace1437bb39d57f19009fd37c945393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.4 MB (864362078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc9669947a4a60029ea0ede28a650cdfb12ae65a681cf74384a57317f7ea72c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 May 2026 05:07:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:07:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:07:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:07:30 GMT
ENV container oci
# Tue, 12 May 2026 05:07:31 GMT
COPY dir:5370c41d6d8459b92eabd7b14d9158353a8d692cfb39a86c0ad6f0e8377d5a95 in /      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:07:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:07:12Z" "org.opencontainers.image.created"="2026-05-12T05:07:12Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:07:12Z
# Tue, 12 May 2026 23:34:28 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 May 2026 23:34:28 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 May 2026 23:35:00 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 23:35:00 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 23:35:00 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 May 2026 23:35:11 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 May 2026 23:35:11 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 May 2026 23:35:11 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:35:11 GMT
ENV SHELL=/bin/bash
# Tue, 12 May 2026 23:35:11 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 May 2026 23:35:12 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 May 2026 23:35:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 May 2026 23:35:12 GMT
LABEL org.label-schema.build-date=2026-05-08T10:08:29.383338563Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3c7c6027c5769d860d87448e2749f4c550a239da org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T10:08:29.383338563Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3c7c6027c5769d860d87448e2749f4c550a239da org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1
# Tue, 12 May 2026 23:35:12 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.1 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 May 2026 23:35:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 23:35:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 May 2026 23:35:12 GMT
CMD ["eswrapper"]
# Tue, 12 May 2026 23:35:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c06b8ad3393fea673394e067fccddfc7ef6d8cee753eba4c4dcd5d67792bfd4b`  
		Last Modified: Tue, 12 May 2026 06:00:36 GMT  
		Size: 40.0 MB (40022633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ceba3fdf125df2e7b15e287d84a2b761aca9f8c7356cd0731e178ccd61dae`  
		Last Modified: Tue, 12 May 2026 23:36:08 GMT  
		Size: 4.3 MB (4278479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f4ee3cd652861bb45dbd98e9766a4627d993bc913161c76b9e3e2b6b4f1e3a`  
		Last Modified: Tue, 12 May 2026 23:36:08 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a712c7bd9766b566a496895f99956ca8f8033cea98c95c402c2cc5c3a9e6454d`  
		Last Modified: Tue, 12 May 2026 23:36:08 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7bdfe223801e75a51a6671cf874ed06c6871b6bf4ba44f7cf89dec547b89b3`  
		Last Modified: Tue, 12 May 2026 23:36:26 GMT  
		Size: 820.0 MB (819971016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348388432bf26c445684483bb19c5fe60704231ae4282aeed547ddc3911b3e00`  
		Last Modified: Tue, 12 May 2026 23:36:09 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da266ce04b38a2a29e4d5a0ea1632c289df4b09a16022ec01ef6bed02b72dd0`  
		Last Modified: Tue, 12 May 2026 23:36:09 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aab7b8dd08d03fde7a6a874b5b7940d85f504769788769372ed9ec7411b16f7`  
		Last Modified: Tue, 12 May 2026 23:36:09 GMT  
		Size: 75.2 KB (75178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e243466473f12747223d9e61764cd18db931bbb288be424f3e8d2334fcc925`  
		Last Modified: Tue, 12 May 2026 23:36:10 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b177d3cca043f98182dab0b47e1ef41d78093384035573fff6fea6f5ab5d569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31441a73f096a4f417b3f8f5281e1fa4cd906185df32e1b6434b887c662e0bdc`

```dockerfile
```

-	Layers:
	-	`sha256:3c4950073e6b417442aea35dbd0d8d8ef9c07289a2efc73b2a1be057ba9df258`  
		Last Modified: Tue, 12 May 2026 23:36:08 GMT  
		Size: 2.4 MB (2390004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e0c03fb0864fbdb27bba9982b74966be489f4c7491c0b81302e6a61c476cc3`  
		Last Modified: Tue, 12 May 2026 23:36:08 GMT  
		Size: 33.8 KB (33776 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.4.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:338b9c6f4251711495b32772e64d29998fe086a281e70a0faa3ea702dac996f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.0 MB (708996304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de6ec3a29670292e5972c3b730182af8a740218183f344b6ac9239e50887fb0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 May 2026 05:08:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:08:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:08:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:08:30 GMT
ENV container oci
# Tue, 12 May 2026 05:08:31 GMT
COPY dir:1ccd99245be3a0b58a1846f076e5b2ceb5e84e683dd2697432c08ac554789d9d in /      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:08:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:08:17Z" "org.opencontainers.image.created"="2026-05-12T05:08:17Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:08:17Z
# Tue, 12 May 2026 23:34:07 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 12 May 2026 23:34:07 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 May 2026 23:35:06 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 23:35:06 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 23:35:06 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 May 2026 23:35:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 12 May 2026 23:35:14 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 12 May 2026 23:35:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:35:14 GMT
ENV SHELL=/bin/bash
# Tue, 12 May 2026 23:35:14 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 May 2026 23:35:14 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 May 2026 23:35:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 May 2026 23:35:14 GMT
LABEL org.label-schema.build-date=2026-05-08T10:08:29.383338563Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3c7c6027c5769d860d87448e2749f4c550a239da org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T10:08:29.383338563Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3c7c6027c5769d860d87448e2749f4c550a239da org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1
# Tue, 12 May 2026 23:35:14 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.4.1 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 12 May 2026 23:35:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 23:35:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 May 2026 23:35:14 GMT
CMD ["eswrapper"]
# Tue, 12 May 2026 23:35:14 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cd21d11a73b4a3fb6683533da05d561785e6bdfe61eb163870493206db32b8fc`  
		Last Modified: Tue, 12 May 2026 06:10:38 GMT  
		Size: 38.2 MB (38205025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d860fe3abf93e4b3153f12d2442c94932ac545432b78fb9adbb2f3187ead7f`  
		Last Modified: Tue, 12 May 2026 23:36:00 GMT  
		Size: 4.3 MB (4282662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c10134553408dfce138c00214429294b894140aefc5cd16653937751071697`  
		Last Modified: Tue, 12 May 2026 23:36:00 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5e13595b3ee9408097668557d4ebe6cd3d7eabeeb05b82deca875fafec25e3`  
		Last Modified: Tue, 12 May 2026 23:36:00 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311cb79f4bbf4f4736eca50ab34d04f7ee311cd1a4e41716534ca1e8a5c6571c`  
		Last Modified: Tue, 12 May 2026 23:36:16 GMT  
		Size: 666.4 MB (666420169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ff6cb2a8cba4303ad8b5a358d32c62f9f05a0ecd74559305b2210a60c04251`  
		Last Modified: Tue, 12 May 2026 23:36:01 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1877744c8dbaffe6b953a7180d00fe7be5a5e81403e03264714b104b2ee2c7d2`  
		Last Modified: Tue, 12 May 2026 23:36:01 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfbc56af938a9654b6e2cc89351706d6eac005516fc7b4a253143543b28ef0`  
		Last Modified: Tue, 12 May 2026 23:36:02 GMT  
		Size: 74.1 KB (74106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de31419acc10b7baf20e3389efbb43b684f8859043b58957696b7dd066e48f69`  
		Last Modified: Tue, 12 May 2026 23:36:02 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.4.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d1e5a130334c76345bfcb23b572ff97a0d44187c2bff777ba9d52e9ed10e5ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb22f0fd341a12b6750d62cd375744809829cc147cf2e24c85fbc2e7cb7133be`

```dockerfile
```

-	Layers:
	-	`sha256:f05e8ba8b4f36cbb6d44c311f0418721596624f7ea7bab53cca305d90dfb25a2`  
		Last Modified: Tue, 12 May 2026 23:36:00 GMT  
		Size: 2.4 MB (2390566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbc23f91bcf32a46a7b7d3d2d2374a2491c1c89b12ca219a441023fbd434634`  
		Last Modified: Tue, 12 May 2026 23:36:00 GMT  
		Size: 34.0 KB (33958 bytes)  
		MIME: application/vnd.in-toto+json
