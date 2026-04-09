<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.14`](#elasticsearch81914)
-	[`elasticsearch:9.2.8`](#elasticsearch928)
-	[`elasticsearch:9.3.3`](#elasticsearch933)

## `elasticsearch:8.19.14`

```console
$ docker pull elasticsearch@sha256:1d7615332ff7ce949eba6b4ac00fd4880a5c493822161bea6d8029caae87d5af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.14` - linux; amd64

```console
$ docker pull elasticsearch@sha256:93697ea11d6529e3edf00998d1a34668034d2734434a68f3ba575e34f7a6f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.9 MB (717862049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e8d115968cbf8662f99bff3bba3729eb3326fa21997b4e80840b8a95048a5b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 17:12:19 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 08 Apr 2026 17:12:20 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 08 Apr 2026 17:12:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:12:20 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 08 Apr 2026 17:12:58 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 08 Apr 2026 17:12:58 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:12:58 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:12:58 GMT
ENV SHELL=/bin/bash
# Wed, 08 Apr 2026 17:12:58 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:12:58 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 08 Apr 2026 17:12:58 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 08 Apr 2026 17:12:59 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 08 Apr 2026 17:12:59 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 08 Apr 2026 17:12:59 GMT
LABEL org.label-schema.build-date=2026-04-02T15:09:12.561504739Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f9adf4c29021dbda28cae7d9c11924471798723d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.14 org.opencontainers.image.created=2026-04-02T15:09:12.561504739Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f9adf4c29021dbda28cae7d9c11924471798723d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.14
# Wed, 08 Apr 2026 17:12:59 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:12:59 GMT
CMD ["eswrapper"]
# Wed, 08 Apr 2026 17:12:59 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f255e079b0cf2699c873825ee1d331483685659c58f5a044ed8023de040f11`  
		Last Modified: Wed, 08 Apr 2026 17:13:51 GMT  
		Size: 7.6 MB (7577253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c685d802f7bc617d1fc3ff268d61df65d1b727c2c1609a581bb8a57535af1bf4`  
		Last Modified: Wed, 08 Apr 2026 17:13:51 GMT  
		Size: 3.5 KB (3539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e5462a35f81a27fd5ae0ae82a672d7ed4825c633869df96183905778df069`  
		Last Modified: Wed, 08 Apr 2026 17:14:10 GMT  
		Size: 680.3 MB (680256395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4506ce94fe20675dc3e6bc3862a3a84545ee2f3b4b3438bfbefdaed92d5a4f`  
		Last Modified: Wed, 08 Apr 2026 17:13:51 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3c5ad8880f772f960c5edd60e3232ca918dcd571f3805d36605b4e35b50478`  
		Last Modified: Wed, 08 Apr 2026 17:13:52 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4d42ab6e289ba3fe0160ea56641ad94fe366de3e5eba8f1bbf13dac7a13668`  
		Last Modified: Wed, 08 Apr 2026 17:13:52 GMT  
		Size: 164.2 KB (164187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d96e1ba0fb92d634208624b6582218092a423aa70888129502af9d4ce7b8b8`  
		Last Modified: Wed, 08 Apr 2026 17:13:53 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65a8fa9790c50123982e9d038547eb8fb2494b11c843c3ec359251acc784a6c`  
		Last Modified: Wed, 08 Apr 2026 17:13:54 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.14` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e512e6959e20b6e68932a636980af26ed3807c483cfad44c15fa772b347d66a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58297908deb943c5a0fce651978d8c63a4ef03d0ed5d870de4959fdf94e844f7`

```dockerfile
```

-	Layers:
	-	`sha256:6afef26ec031ac63f9becc3d65c76c0c30b6aacf46c379daf5a99723a264ddd7`  
		Last Modified: Wed, 08 Apr 2026 17:13:51 GMT  
		Size: 3.2 MB (3208984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e25bce3f96351f2d1d5c1791a6d941b8afae066546a22fbdb3e2bbc60fa9b9`  
		Last Modified: Wed, 08 Apr 2026 17:13:50 GMT  
		Size: 36.8 KB (36816 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.14` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d4b5df9b1d6c63875f572db369700b1f0b109f777a45aaf7bab9c186738160ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.6 MB (565552605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2572c67649195b0cf5f8e419051d8ac91251e73e18c783a02480ec4d91cf0b3`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 17:09:40 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 08 Apr 2026 17:09:41 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 08 Apr 2026 17:09:41 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:09:41 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 08 Apr 2026 17:10:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 08 Apr 2026 17:10:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:10:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:10:24 GMT
ENV SHELL=/bin/bash
# Wed, 08 Apr 2026 17:10:24 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:10:24 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 08 Apr 2026 17:10:24 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 08 Apr 2026 17:10:24 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 08 Apr 2026 17:10:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 08 Apr 2026 17:10:24 GMT
LABEL org.label-schema.build-date=2026-04-02T15:09:12.561504739Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f9adf4c29021dbda28cae7d9c11924471798723d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.14 org.opencontainers.image.created=2026-04-02T15:09:12.561504739Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f9adf4c29021dbda28cae7d9c11924471798723d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.14
# Wed, 08 Apr 2026 17:10:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:10:24 GMT
CMD ["eswrapper"]
# Wed, 08 Apr 2026 17:10:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e65bb0dd8eda8a5c7978666efb6dfe4a261e7f5a1c2420833ded9464c436c71`  
		Last Modified: Wed, 08 Apr 2026 17:11:04 GMT  
		Size: 7.4 MB (7394300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2de25a70bf194e096b7096986736da7b732436df12292f4a873a31e19f3eb7`  
		Last Modified: Wed, 08 Apr 2026 17:11:03 GMT  
		Size: 3.5 KB (3530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776bc911bb249406df1dd41ab58c1c5e6257ba21a0fca2b1f4697abc31b52090`  
		Last Modified: Wed, 08 Apr 2026 17:11:16 GMT  
		Size: 529.0 MB (528993219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344b325cef95b97673e866743817cd7ff8c37fb8fab9422b45244d6f876cc430`  
		Last Modified: Wed, 08 Apr 2026 17:11:03 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554c1b9e27fb51a693367b2b352b323204e142fc63ced5339e0d3942a45dc0a9`  
		Last Modified: Wed, 08 Apr 2026 17:11:05 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc28f0a7d67dc026f5b7fb0b3cec077b4926989155a97a392cc174f13a509e3`  
		Last Modified: Wed, 08 Apr 2026 17:11:05 GMT  
		Size: 160.7 KB (160693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0992920034de354edf227fe6073e7bf9b8b23e138e932987267b504ca671a0cc`  
		Last Modified: Wed, 08 Apr 2026 17:11:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b016f3a2b835d6ab16d8b4015279421b27f1c4358fb2a41a023313882cb692`  
		Last Modified: Wed, 08 Apr 2026 17:11:06 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.14` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8d3ee5cb294816b172594a03e6815b3a764f78e3fe900f534709522002bd9016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4aa3ba636310cc9cb68e38c78079802f7a1aa51b37b63deadb7bedba510527`

```dockerfile
```

-	Layers:
	-	`sha256:bdedbd6b691d4d809b5819cc7e52e762631fcafbadc8c091a06ea990340b1353`  
		Last Modified: Wed, 08 Apr 2026 17:11:04 GMT  
		Size: 3.2 MB (3209397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fb995b3fdccbd591fdc1f97a6aebbf668cad263b28079c96e9d18fcc31172b`  
		Last Modified: Wed, 08 Apr 2026 17:11:03 GMT  
		Size: 37.0 KB (37018 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.8`

```console
$ docker pull elasticsearch@sha256:fa720841530fbbd446aea2a3a54acd74d7fbfabe1e74adf737d1997c40343f4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:49af78a160c051f4209c48eedd03bc2a9efe756e59750a1d1317a17e9a937e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.5 MB (738467895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84155a7b77dd78217e66763d801dd102478042c8ee294513839fd48dcfa48a07`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:29:48 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:29:48 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 08 Apr 2026 17:30:14 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:30:14 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:30:14 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 08 Apr 2026 17:30:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 08 Apr 2026 17:30:24 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 08 Apr 2026 17:30:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:30:24 GMT
ENV SHELL=/bin/bash
# Wed, 08 Apr 2026 17:30:24 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:30:24 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 08 Apr 2026 17:30:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 08 Apr 2026 17:30:24 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 08 Apr 2026 17:30:24 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 08 Apr 2026 17:30:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 08 Apr 2026 17:30:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:30:25 GMT
CMD ["eswrapper"]
# Wed, 08 Apr 2026 17:30:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3e735208f776d9c8f950b7bb45dfd9edf70c91eafea3af8140f3f24d8c9024`  
		Last Modified: Wed, 08 Apr 2026 17:31:16 GMT  
		Size: 4.3 MB (4277751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9583c59ded582e0aac7d80a23b3fdcd22ab4636a610f022a92b0964b58c88ba`  
		Last Modified: Wed, 08 Apr 2026 17:31:16 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c581be82c9204559f09a710c372f03a8a0c3cc79beede30bfe38dcd6446ea`  
		Last Modified: Wed, 08 Apr 2026 17:31:16 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fe2506d851a2f5efde2e3b6cc4f99c7db75f274bf82372680fb76d33b63b84`  
		Last Modified: Wed, 08 Apr 2026 17:31:32 GMT  
		Size: 694.1 MB (694117560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6025e1581bb2075cc910b2b1a0a1cae99a228411493a06c33446c48ce5e951d4`  
		Last Modified: Wed, 08 Apr 2026 17:31:17 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4013b1fd4dfc88527165c3bc13baa16b0a97c800d64046bf0ce3c17fe13dafae`  
		Last Modified: Wed, 08 Apr 2026 17:31:17 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4750d14cbd5fac92af34ca160c33e0a5c836cbfd60d31fa798ee4040a8767acd`  
		Last Modified: Wed, 08 Apr 2026 17:31:17 GMT  
		Size: 75.2 KB (75178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079c8f245a88e01ca2a397dfeddb7f812005c9e606676139d34b77270cbb66fa`  
		Last Modified: Wed, 08 Apr 2026 17:31:18 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b3b498d8cb3a79a646e03d905f87ccddc994b7297d1f88c7de245e7e957f7ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f5a4a40ba1417c4d69f94deed0468c11a5e64a8fb6e22c685a862860e5fadc`

```dockerfile
```

-	Layers:
	-	`sha256:e9067bdff95ca3d9d90f1f395ebcdb3a9b342f763aeb52980b8876d9956b5c02`  
		Last Modified: Wed, 08 Apr 2026 17:31:16 GMT  
		Size: 2.1 MB (2098149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:160f91d26482f6eb299614ad8aef1a4a1176d871c9c1d64a2cbf196c43a8be7c`  
		Last Modified: Wed, 08 Apr 2026 17:31:16 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e1afaa51fdcdfb2915f40e8c7155b5c3d43e219cd07d8ccd98c360500596087e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.5 MB (582513105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e8b5120829828e0d83102f02bf60187621a7e2d59db9285cba57cb300a3c2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:55:31 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:32 GMT
COPY dir:e3968b666ccf8b1da827a1f934e7d66b38ad6335b0bf20a2a01583a6f9f3fdaa in /      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:33 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:55:18Z" "org.opencontainers.image.created"="2026-04-08T04:55:18Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:55:18Z
# Wed, 08 Apr 2026 17:28:25 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:28:25 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 08 Apr 2026 17:29:18 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:29:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:29:18 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 08 Apr 2026 17:29:25 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 08 Apr 2026 17:29:25 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 08 Apr 2026 17:29:25 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:29:25 GMT
ENV SHELL=/bin/bash
# Wed, 08 Apr 2026 17:29:25 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:29:25 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 08 Apr 2026 17:29:25 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 08 Apr 2026 17:29:25 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 08 Apr 2026 17:29:25 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 08 Apr 2026 17:29:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 08 Apr 2026 17:29:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:29:25 GMT
CMD ["eswrapper"]
# Wed, 08 Apr 2026 17:29:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1ffb0d1826b0600c6d4836c7ada23756af4c1475452e12ce1bed713d58738262`  
		Last Modified: Wed, 08 Apr 2026 05:41:58 GMT  
		Size: 38.2 MB (38200278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c69c90594beb420ae706f7e3ae6a24c5b1f75a6e6bdf32b15e1f96b93fbe73f`  
		Last Modified: Wed, 08 Apr 2026 17:30:04 GMT  
		Size: 4.3 MB (4286296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4652cc60302f01cb0ce9ac57442d9586a519fba35feb43790f939bbddc1623f4`  
		Last Modified: Wed, 08 Apr 2026 17:30:04 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c190b9cfa22d695f2e06aa66b961f0d657e33f805626408cb3c76de585cbabf6`  
		Last Modified: Wed, 08 Apr 2026 17:30:04 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bc4b3e7b31c88f960fd1e9c039c1c05f577529f514b357baa8aef5f5cecd54`  
		Last Modified: Wed, 08 Apr 2026 17:30:16 GMT  
		Size: 539.9 MB (539938077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b97e3e3d3a23c429881efcd8b58c99cd6e64e4c1599cadee91a93696dc138b`  
		Last Modified: Wed, 08 Apr 2026 17:30:05 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3e8cc73214ab3011c800ec451b5e4d6a72a37f53ab733f2842ef8558b0cb32`  
		Last Modified: Wed, 08 Apr 2026 17:30:05 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226af9746bfd5c4603eb0f1497267d03dfc4d78b001817a22612c82c0d47a4f5`  
		Last Modified: Wed, 08 Apr 2026 17:30:05 GMT  
		Size: 74.1 KB (74109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6a29ead44466413a53ec6c8825c2f93a90d4424edc0351b9ededdcecfac124`  
		Last Modified: Wed, 08 Apr 2026 17:30:06 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:69e7dd7f2f3ac66f072201d336e0ef998491f530c96b00061c5f973b336acfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f330ba0e26ea567827b70e316110f8a7a0f29c62cc68526fd941a085593cd7`

```dockerfile
```

-	Layers:
	-	`sha256:b6c6804b1a0f0a5bffc7baa7c890c98e8926daeed597326485023d5314886a2f`  
		Last Modified: Wed, 08 Apr 2026 17:30:04 GMT  
		Size: 2.1 MB (2098711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b7f5ba832267545713bb9cecd57e567dfe4e788a5314a1e5007e8f3e2fb2c9`  
		Last Modified: Wed, 08 Apr 2026 17:30:03 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.3`

```console
$ docker pull elasticsearch@sha256:afbc1f1435483cd8bd201329a7250bb779f587ba199d34aec167088309cebfca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:88fffeb5d08fe55bea1dacb11f8abc1205241b5b32ad4a22c14f85e578d9a90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716652142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f61801e89a9e45fa13f3e47902ff9270a0dc11a1999f6893cb2a8c3672c4b58`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:29:16 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:29:16 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 08 Apr 2026 17:30:00 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:30:00 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:30:00 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 08 Apr 2026 17:30:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 08 Apr 2026 17:30:10 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 08 Apr 2026 17:30:10 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:30:10 GMT
ENV SHELL=/bin/bash
# Wed, 08 Apr 2026 17:30:10 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:30:10 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 08 Apr 2026 17:30:10 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 08 Apr 2026 17:30:10 GMT
LABEL org.label-schema.build-date=2026-04-01T22:08:18.783399214Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T22:08:18.783399214Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Wed, 08 Apr 2026 17:30:10 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 08 Apr 2026 17:30:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 08 Apr 2026 17:30:10 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:30:10 GMT
CMD ["eswrapper"]
# Wed, 08 Apr 2026 17:30:10 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffa67faaa2ba4a2002e3dd7911e897ccaa9c26c0c7a5aded09e72437c1224f7`  
		Last Modified: Wed, 08 Apr 2026 17:31:02 GMT  
		Size: 4.3 MB (4277739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f2ccba1d04e3a63ae62d173845c2f8d525bd80e61ddffbbd0a22dbd5c3cab7`  
		Last Modified: Wed, 08 Apr 2026 17:31:02 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffbdfe847dcbdaa3bf746fd08b673386f13a02b5799443cc746648e39a6525a`  
		Last Modified: Wed, 08 Apr 2026 17:31:02 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450c1c7eb770e25c3696960ecdf1bfbb9e8a93b9206e8ab7d5eab25e37ee0671`  
		Last Modified: Wed, 08 Apr 2026 17:31:16 GMT  
		Size: 672.3 MB (672301808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120bd0372092a90005c70ea5fa6a7bbb18d9626e356708d8e35e76c80a7d41d8`  
		Last Modified: Wed, 08 Apr 2026 17:31:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f539a157d4ec518f930be0a6b7d38e37e80b74dbacd4cc74b5161492ad306d96`  
		Last Modified: Wed, 08 Apr 2026 17:31:03 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54664451ba41b1b1c0140a7e0c7321a55641890a7494a5e486c7c933a2a73e3a`  
		Last Modified: Wed, 08 Apr 2026 17:31:04 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cbd0d8fbd3834ec399215cf94616ea3661aacc3d491138c05cae3ba65e1e24`  
		Last Modified: Wed, 08 Apr 2026 17:31:05 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8186d2500820f0317c14fee04d24220f1a41c82c81381b4c3f891cb8acc3b3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b6537310d0b57c6a35ac9f9d1fc851009342ab16ebff3c33587b6b13db95d3`

```dockerfile
```

-	Layers:
	-	`sha256:38810c9c9808f3c3e91ddce840ca87c607ac072cbec741fedb423d63989781f5`  
		Last Modified: Wed, 08 Apr 2026 17:31:02 GMT  
		Size: 2.1 MB (2089789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8713fa200a30b5b0274558aa4a6d09888cb0be31a6c216d1e23fa8892b14d7c0`  
		Last Modified: Wed, 08 Apr 2026 17:31:02 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:2fb63fc5655ae4fd1bfff09327b83f31c62dc9c96b91ee8f5f1342f7c83d517a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.7 MB (560691078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a2aff9ba99fbe2b2f7401f409c8e2841e37e046fa98ef3dc24e10e69faaff8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:55:31 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:32 GMT
COPY dir:e3968b666ccf8b1da827a1f934e7d66b38ad6335b0bf20a2a01583a6f9f3fdaa in /      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:33 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:55:18Z" "org.opencontainers.image.created"="2026-04-08T04:55:18Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:55:18Z
# Wed, 08 Apr 2026 17:28:37 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:28:37 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 08 Apr 2026 17:29:32 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:29:32 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:29:32 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 08 Apr 2026 17:29:38 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 08 Apr 2026 17:29:38 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 08 Apr 2026 17:29:38 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:29:38 GMT
ENV SHELL=/bin/bash
# Wed, 08 Apr 2026 17:29:38 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:29:38 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 08 Apr 2026 17:29:38 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 08 Apr 2026 17:29:38 GMT
LABEL org.label-schema.build-date=2026-04-01T22:08:18.783399214Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T22:08:18.783399214Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Wed, 08 Apr 2026 17:29:38 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 08 Apr 2026 17:29:38 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 08 Apr 2026 17:29:38 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 08 Apr 2026 17:29:38 GMT
CMD ["eswrapper"]
# Wed, 08 Apr 2026 17:29:38 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1ffb0d1826b0600c6d4836c7ada23756af4c1475452e12ce1bed713d58738262`  
		Last Modified: Wed, 08 Apr 2026 05:41:58 GMT  
		Size: 38.2 MB (38200278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeec99b135547f49e21ecc74ca06d4b9fbc369706e6d72a5ec177a4312f8105`  
		Last Modified: Wed, 08 Apr 2026 17:30:17 GMT  
		Size: 4.3 MB (4286295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaffbfb428f1e434b367f34ad7d3174790c703584c1fe20fd836d8e003b9456d`  
		Last Modified: Wed, 08 Apr 2026 17:30:17 GMT  
		Size: 1.5 KB (1524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccaaa287bc5db2e5a90459b6b45a659c4d6fa40a1b018b71c5b3e7e49b6f308`  
		Last Modified: Wed, 08 Apr 2026 17:30:17 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afee6f71e978d008d74811b4a0d47526c8ac64f467dcd0d3b9be538a642ead9`  
		Last Modified: Wed, 08 Apr 2026 17:30:29 GMT  
		Size: 518.1 MB (518116062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bd89c2486d94bf55ce21b0f7855acb11b3561b84d65eeb8749c35b2eaee9a9`  
		Last Modified: Wed, 08 Apr 2026 17:30:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ef974d8856161d58577a60d545626e28101f481cb443f1812656b8c21ae30`  
		Last Modified: Wed, 08 Apr 2026 17:30:19 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524d3f5d3d8391d80604f1c02a6d810589308bf457ae0387c87a5f3ea399377`  
		Last Modified: Wed, 08 Apr 2026 17:30:19 GMT  
		Size: 74.1 KB (74103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365525db301eceee7d50e5ad3b73a4008fc08aa681e7ce7364a679603d9cc8c1`  
		Last Modified: Wed, 08 Apr 2026 17:30:20 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:dcb39eddcd516ff1024a3129fe05c2cc28e4e4e1aefe2a1e76d6597d1cc6e9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884726b472fb6c8446362714118cb612634346bcd55f12f4b0e9bad4e1d70c13`

```dockerfile
```

-	Layers:
	-	`sha256:bbb378355297cf79ceb707e07611cb51c471e28c29eeac1b01d37801a350342b`  
		Last Modified: Wed, 08 Apr 2026 17:30:17 GMT  
		Size: 2.1 MB (2090351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e080da45c3a5a23059b1a36b64283ce4d30138060c4a480b1df1f8535ad76d30`  
		Last Modified: Wed, 08 Apr 2026 17:30:17 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
