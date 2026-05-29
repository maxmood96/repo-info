<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.16`](#elasticsearch81916)
-	[`elasticsearch:9.3.5`](#elasticsearch935)
-	[`elasticsearch:9.4.2`](#elasticsearch942)

## `elasticsearch:8.19.16`

```console
$ docker pull elasticsearch@sha256:832cb4df76ba2a08f0051742d216a67e3e3a7d8a616082793ed0150a95d3c9fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.16` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d1d19fef8b5dc5f45baac53fdc633e443094cb6d38f3a8c54eee0495e1f95413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.7 MB (721725700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7da5960a81f5b2b4121abbf1815dbf9536dfdec972e24456b77be4cbbd6a41`
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
# Thu, 28 May 2026 21:34:05 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 May 2026 21:34:06 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 May 2026 21:34:06 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:34:06 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2026 21:35:30 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 May 2026 21:35:30 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:35:30 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:35:30 GMT
ENV SHELL=/bin/bash
# Thu, 28 May 2026 21:35:30 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 May 2026 21:35:30 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 May 2026 21:35:30 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 May 2026 21:35:30 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 May 2026 21:35:30 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 May 2026 21:35:30 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:50.658641519Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0ecfe314ed6ddebb736091bf37b3b6758209b73b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.16 org.opencontainers.image.created=2026-05-25T22:10:50.658641519Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0ecfe314ed6ddebb736091bf37b3b6758209b73b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.16
# Thu, 28 May 2026 21:35:30 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2026 21:35:30 GMT
CMD ["eswrapper"]
# Thu, 28 May 2026 21:35:30 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14b2dc719a912fd7bd1405e40b4ddb390a2813645626156ecc64f91b2df773f`  
		Last Modified: Thu, 28 May 2026 21:36:23 GMT  
		Size: 6.7 MB (6683940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdea0ef0992eece25e38f8eb7816713c9168808af5013028261cadfd3c1931f5`  
		Last Modified: Thu, 28 May 2026 21:36:23 GMT  
		Size: 3.5 KB (3531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1942f8cd1136dc1f35da3899a4e76a8426b093451e3af59d1f15c083749b9a78`  
		Last Modified: Thu, 28 May 2026 21:36:36 GMT  
		Size: 685.0 MB (685013841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185cbde627e92a32374062a0689ea6d84ff64202f7600af1663663674ebb4fbf`  
		Last Modified: Thu, 28 May 2026 21:36:23 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a3fbc12c3b7298d67cb046c1c0dd4216fa00428641c9eaff9be30781c03d95`  
		Last Modified: Thu, 28 May 2026 21:36:24 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a561dc1b1dc753b605380324d7284ce920503a10743b514f7e3d6b75da7e5eab`  
		Last Modified: Thu, 28 May 2026 21:36:24 GMT  
		Size: 164.2 KB (164189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779f13d41efd8805066bf438af1e6903c6f3727a7e753f8ba5cdedf325446df7`  
		Last Modified: Thu, 28 May 2026 21:36:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e93a2ba1094c012077a9e2795035cbb0eb24e21df6b8df257b53415547996`  
		Last Modified: Thu, 28 May 2026 21:36:26 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.16` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:30da7b39673d8f703eda67ba8c6a4c0893dd3daa98369dc9749030ab7f53fcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3244133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590f5000123042d48684a9ddcb1dc8bc653ebcd99b2de34712b4cc75c454c451`

```dockerfile
```

-	Layers:
	-	`sha256:affae8cebf049fd8c2b471ad89ce4cc79500f7b3598d9761481f607f5b475414`  
		Last Modified: Thu, 28 May 2026 21:36:23 GMT  
		Size: 3.2 MB (3207317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4016182e6cc0298e24c83bcfac8ab1c7bd70448398870105cf43d42c0e731f53`  
		Last Modified: Thu, 28 May 2026 21:36:23 GMT  
		Size: 36.8 KB (36816 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.16` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:f8f705ae7c4c577f4dd7eb892c8b559ba6d1b8f40b2f836391bf51ed40b3261b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.6 MB (569552944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61375056b5cd58b5522f7aab8f039b3706e9f11dbadd87ae0556f041cf049ff`
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
# Thu, 28 May 2026 21:33:27 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 May 2026 21:33:27 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 May 2026 21:33:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:33:27 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 May 2026 21:34:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 May 2026 21:34:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:34:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:34:09 GMT
ENV SHELL=/bin/bash
# Thu, 28 May 2026 21:34:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 May 2026 21:34:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 May 2026 21:34:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 May 2026 21:34:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 May 2026 21:34:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 May 2026 21:34:09 GMT
LABEL org.label-schema.build-date=2026-05-25T22:10:50.658641519Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0ecfe314ed6ddebb736091bf37b3b6758209b73b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.16 org.opencontainers.image.created=2026-05-25T22:10:50.658641519Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0ecfe314ed6ddebb736091bf37b3b6758209b73b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.16
# Thu, 28 May 2026 21:34:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 May 2026 21:34:09 GMT
CMD ["eswrapper"]
# Thu, 28 May 2026 21:34:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb382ea9b4f75132154df35e22cffa81b74b1a4f195a90c9464bb37a0e15ea45`  
		Last Modified: Thu, 28 May 2026 21:34:48 GMT  
		Size: 6.6 MB (6571816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2474d22c8128e964d92834410e2c07a06564171bf475ed0751317efc2f46ff`  
		Last Modified: Thu, 28 May 2026 21:34:48 GMT  
		Size: 3.5 KB (3523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0554b61cf1296de39393227b04b498b91ac497e1caf656f684fe31539806d37`  
		Last Modified: Thu, 28 May 2026 21:34:59 GMT  
		Size: 533.8 MB (533814321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de966a6a5de94381a9497aeaa4db6eea504ee34cff8a9ea352494f681fe6bc1`  
		Last Modified: Thu, 28 May 2026 21:34:48 GMT  
		Size: 9.1 KB (9107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb287e63b6aa331cacb7edc638701f9815fbb3d63cf147bb97a08a1394e0013`  
		Last Modified: Thu, 28 May 2026 21:34:50 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543b75a820a0136351476598379b050e1aa779fdfce40dd0c0d55e82a501e0b5`  
		Last Modified: Thu, 28 May 2026 21:34:49 GMT  
		Size: 160.7 KB (160704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa03c7b9e6189831c910bc5a9e2917fd6d75e95c7a4ee2295b30a10315217cc`  
		Last Modified: Thu, 28 May 2026 21:34:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54150a4c3a0bf1a4c1b3bc38a015f5ba05e1bf77c351dece25b0ff0c7dad605d`  
		Last Modified: Thu, 28 May 2026 21:34:51 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.16` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d7c6151fc15e20421287751f4fa26558bcda7f3e4911165c285a94f24718bbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3244749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c728f37ec5bfc58fd40996ef63ef1862ab86ed69ecce2271d3a85cf103df4ddf`

```dockerfile
```

-	Layers:
	-	`sha256:22c6cf82b7cc780d75bc3bb43522496f29ac3f794002b64e335f3b9490a1e1f6`  
		Last Modified: Thu, 28 May 2026 21:34:48 GMT  
		Size: 3.2 MB (3207730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a24cb2c1e3f7acf0285dbc6dc4c99a04f819e401938dc7e4ea1eb60504e771`  
		Last Modified: Thu, 28 May 2026 21:34:48 GMT  
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
