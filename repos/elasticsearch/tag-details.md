<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.13`](#elasticsearch81913)
-	[`elasticsearch:9.2.7`](#elasticsearch927)
-	[`elasticsearch:9.3.2`](#elasticsearch932)

## `elasticsearch:8.19.13`

```console
$ docker pull elasticsearch@sha256:dbcd3f1bdf627ffefa3a1f98e5cdfc85de4fe00e510f38f901fe49225e1515e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.13` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5df68d09563b2a2970034f9180dfe46f5653e76670199733bd1116d513b63b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.9 MB (718861308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa07ec55c493c5a32caf7342d95e226099fd86324234bc4f916af8f99c59c02`
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
# Thu, 19 Mar 2026 23:58:40 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 19 Mar 2026 23:58:40 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 19 Mar 2026 23:58:40 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 19 Mar 2026 23:58:40 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 19 Mar 2026 23:59:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 19 Mar 2026 23:59:33 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 19 Mar 2026 23:59:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Mar 2026 23:59:33 GMT
ENV SHELL=/bin/bash
# Thu, 19 Mar 2026 23:59:33 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 19 Mar 2026 23:59:33 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 19 Mar 2026 23:59:33 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 19 Mar 2026 23:59:34 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 19 Mar 2026 23:59:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 19 Mar 2026 23:59:34 GMT
LABEL org.label-schema.build-date=2026-03-16T10:08:32.007626438Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f6279a2167a248af2bb287409231fb0cf52aa0db org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.13 org.opencontainers.image.created=2026-03-16T10:08:32.007626438Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f6279a2167a248af2bb287409231fb0cf52aa0db org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.13
# Thu, 19 Mar 2026 23:59:34 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Mar 2026 23:59:34 GMT
CMD ["eswrapper"]
# Thu, 19 Mar 2026 23:59:34 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b448b728ee80965af978ded24b634eed6cc3de0cac8422480b74a0ecfe6fb41d`  
		Last Modified: Fri, 20 Mar 2026 00:00:29 GMT  
		Size: 8.6 MB (8598306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874131b708bf73c2c2b5a2b772eb0459e5d5c19d74068ecc897c0298994638d4`  
		Last Modified: Fri, 20 Mar 2026 00:00:29 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da63532ac26fc2508f644397b755f78a6c9584157767f958906ffa9548556391`  
		Last Modified: Fri, 20 Mar 2026 00:00:42 GMT  
		Size: 680.2 MB (680236080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb40a6eca61876641227f0623f0c63cc0106a61c98fa01eb6216480bdc4c9681`  
		Last Modified: Fri, 20 Mar 2026 00:00:30 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ba4bc1ce49bf1aa9aa4f17d2c303c4f593da79c8d65f876e397df6063acbeb`  
		Last Modified: Fri, 20 Mar 2026 00:00:30 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ae6037294f2f296410d88d00c93f1949aa140c5e247cb6b3ec8f4ee7e0fb89`  
		Last Modified: Fri, 20 Mar 2026 00:00:32 GMT  
		Size: 164.2 KB (164188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb75a47611640205793191b5d23a56b10b5fe393bc6417f5620d5367429f833`  
		Last Modified: Fri, 20 Mar 2026 00:00:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0572ba0ec15da3d2d9a5814d536c085af808f6d4b8606bfe5ddc2347678091a5`  
		Last Modified: Fri, 20 Mar 2026 00:00:35 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.13` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:204bfa404fbcee19a3030da5747bef6f3281934473cd3e5470a945b84b11f437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219c65e375d790d904f194842ba9984883ef321095b86babf049cc158872cf74`

```dockerfile
```

-	Layers:
	-	`sha256:140241e074225a7668df370cd137246b9493de42a48064c39704071bb26f6793`  
		Last Modified: Fri, 20 Mar 2026 00:00:29 GMT  
		Size: 3.2 MB (3208984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba13cc0c156c0653c246c4ea11a5a1b209a4be6da8b69983c625d68e9f685f4e`  
		Last Modified: Fri, 20 Mar 2026 00:00:29 GMT  
		Size: 36.8 KB (36816 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.13` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e343aa267e4c73b4b3ba61ae0341a00c18f1e6400fba7280ca8046cc1d50ced7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.8 MB (566759897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a39f6d9d2582547cae9b6570cacc7ab1f87cb447c090bbaab3a9f03b525cc7b`
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
# Thu, 19 Mar 2026 23:58:46 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 19 Mar 2026 23:58:46 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 19 Mar 2026 23:58:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 19 Mar 2026 23:58:46 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 19 Mar 2026 23:59:22 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 19 Mar 2026 23:59:22 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 19 Mar 2026 23:59:22 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Mar 2026 23:59:22 GMT
ENV SHELL=/bin/bash
# Thu, 19 Mar 2026 23:59:22 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 19 Mar 2026 23:59:22 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 19 Mar 2026 23:59:22 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 19 Mar 2026 23:59:23 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 19 Mar 2026 23:59:23 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 19 Mar 2026 23:59:23 GMT
LABEL org.label-schema.build-date=2026-03-16T10:08:32.007626438Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f6279a2167a248af2bb287409231fb0cf52aa0db org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.13 org.opencontainers.image.created=2026-03-16T10:08:32.007626438Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f6279a2167a248af2bb287409231fb0cf52aa0db org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.13
# Thu, 19 Mar 2026 23:59:23 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 19 Mar 2026 23:59:23 GMT
CMD ["eswrapper"]
# Thu, 19 Mar 2026 23:59:23 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c13472ec15d2a93b41251d52c5a006525d579123d5086fd492852c5ed253412`  
		Last Modified: Fri, 20 Mar 2026 00:00:02 GMT  
		Size: 8.6 MB (8628319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4cb55eaddb26df6fd915eb5776f1e2e9579d93df48bd4427b00481de4d8325`  
		Last Modified: Fri, 20 Mar 2026 00:00:01 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b03bb4a07440bbd972a3bb436118b931545d68f98470ba03cdb25c32dabfe71`  
		Last Modified: Fri, 20 Mar 2026 00:00:16 GMT  
		Size: 529.0 MB (528970871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa186de3bebc22a69ae030afd596725413bdbf8f25ac750a5dd72e99b4a397`  
		Last Modified: Fri, 20 Mar 2026 00:00:01 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6ef2db0ae69eacf4d546deb7e2c7c6342d1e77f7276b21fa9924897d7895f8`  
		Last Modified: Fri, 20 Mar 2026 00:00:04 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1126f8621be6ba7b6be4ce082d779e316221d9d0d1f09c4dcd5d3780d31e6cc0`  
		Last Modified: Fri, 20 Mar 2026 00:00:05 GMT  
		Size: 160.7 KB (160684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea992f0a61dedba8efbaf4848fcacc4bf001bafa22057db4035b20d11425661f`  
		Last Modified: Fri, 20 Mar 2026 00:00:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567288c6bdac8d2710e2bf40f2fe3f4e2b819a93b5f2847bf38826bb7b52a4ab`  
		Last Modified: Fri, 20 Mar 2026 00:00:09 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.13` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:83373b4991e8f992ab6acd6f4b028b4c088dba3f2e48fceb1e17a31b8ece4caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d2889bdff259ca782a4b59159cf56e76caa1a1ee044b16b074d2089d0bd9c3`

```dockerfile
```

-	Layers:
	-	`sha256:a241ef2b4fc203e4890acb80907b13861df81e7e8503e8fff0605d4e2efd32d8`  
		Last Modified: Fri, 20 Mar 2026 00:00:01 GMT  
		Size: 3.2 MB (3209397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21c8072f6bfc7f76245b61dac6db34f03e5556240bc943f17b899be7d5337ed`  
		Last Modified: Fri, 20 Mar 2026 00:00:01 GMT  
		Size: 37.0 KB (37019 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.7`

```console
$ docker pull elasticsearch@sha256:aa13b7529ab4ebcb3a6a5f614e65483e46955275ef49a6ba31afc042cd2d2ee2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:036e93cf03f45efba1c67db2994c74ac64a490224fd92c68997f98c1a96395cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.5 MB (738504783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7811bb6860aef1973ac47893dfc69ae645f9abf407d4ca25b6021de3678cdc`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:17:59 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:18:00 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 20 Mar 2026 00:19:16 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:19:16 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 20 Mar 2026 00:19:16 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 20 Mar 2026 00:19:25 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 20 Mar 2026 00:19:26 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 20 Mar 2026 00:19:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:19:26 GMT
ENV SHELL=/bin/bash
# Fri, 20 Mar 2026 00:19:26 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:19:26 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 20 Mar 2026 00:19:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 20 Mar 2026 00:19:26 GMT
LABEL org.label-schema.build-date=2026-03-16T13:06:33.885743581Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=39e49969374b9cb20b84dc00f7d505d67480deeb org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.7 org.opencontainers.image.created=2026-03-16T13:06:33.885743581Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=39e49969374b9cb20b84dc00f7d505d67480deeb org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.7
# Fri, 20 Mar 2026 00:19:26 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.7 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 20 Mar 2026 00:19:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 20 Mar 2026 00:19:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:19:26 GMT
CMD ["eswrapper"]
# Fri, 20 Mar 2026 00:19:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802b018df7db3bdc8700ca77e8be0d36aeb73fcd63f158ed64725554cf78f485`  
		Last Modified: Fri, 20 Mar 2026 00:20:19 GMT  
		Size: 4.3 MB (4282170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dcc6ccd75fb71534ac6c46537f591e9bbe39ca53853ea734831a636724ec4a`  
		Last Modified: Fri, 20 Mar 2026 00:20:19 GMT  
		Size: 1.5 KB (1541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8602969bfd708fc6d5f47affe0aa6fd9ed25db066086cf5ce597fbf2b2dda190`  
		Last Modified: Fri, 20 Mar 2026 00:20:19 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2ca21172fc24ac771774598bbe865c0f0493be279415549e70160a2b5b7b3c`  
		Last Modified: Fri, 20 Mar 2026 00:20:32 GMT  
		Size: 694.1 MB (694101526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7b3bd3a4865a67962e7e418b8deb8ca5a836df6c40b9238a993a1bd7868c00`  
		Last Modified: Fri, 20 Mar 2026 00:20:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692b6940b62b37cdc8add56a27491de6d852f59615365a7561b618ce7a4433b1`  
		Last Modified: Fri, 20 Mar 2026 00:20:20 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414ff37b61c63e68170e08c1d9a289e125ecdf20511cefe48f6816beed19a46`  
		Last Modified: Fri, 20 Mar 2026 00:20:20 GMT  
		Size: 75.2 KB (75184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34fdbd274842907851b82f6337b87386e4f031939199c9bddc3b0c2fd03e271`  
		Last Modified: Fri, 20 Mar 2026 00:20:21 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:04be870bb6de344dbade85301bc5f31caded4dfd7cfbfab26a14409cf51270bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b9573a954fa2655bed02027a59af7d8b683aaa9c5306e53e1bc2062a4a34ec`

```dockerfile
```

-	Layers:
	-	`sha256:1235055924d7a09a6eb1614916e3953007c0bb7a39752ae37d50a4112da616a4`  
		Last Modified: Fri, 20 Mar 2026 00:20:19 GMT  
		Size: 2.1 MB (2098149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b6ea0bf9072352a948318430051efa0db89b676aa33ef3349e884d23f98fa93`  
		Last Modified: Fri, 20 Mar 2026 00:20:19 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:38c16096db91d8751f8f905fa1ac868add554bd7b9165e02e2f216f69972116c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.5 MB (582518757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6838fba6b9d0b6cd502efa90db950c424e2ac1122421c495c2953f05ce334d60`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:15:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:15:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 20 Mar 2026 00:16:21 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:16:21 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 20 Mar 2026 00:16:21 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 20 Mar 2026 00:16:27 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 20 Mar 2026 00:16:27 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 20 Mar 2026 00:16:27 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:16:27 GMT
ENV SHELL=/bin/bash
# Fri, 20 Mar 2026 00:16:27 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:16:28 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 20 Mar 2026 00:16:28 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 20 Mar 2026 00:16:28 GMT
LABEL org.label-schema.build-date=2026-03-16T13:06:33.885743581Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=39e49969374b9cb20b84dc00f7d505d67480deeb org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.7 org.opencontainers.image.created=2026-03-16T13:06:33.885743581Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=39e49969374b9cb20b84dc00f7d505d67480deeb org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.7
# Fri, 20 Mar 2026 00:16:28 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.7 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 20 Mar 2026 00:16:28 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 20 Mar 2026 00:16:28 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:16:28 GMT
CMD ["eswrapper"]
# Fri, 20 Mar 2026 00:16:28 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3b3b5847fe25c27febbadd71588acda2aabd8cfea31c8ba6354d173f5e42ca`  
		Last Modified: Fri, 20 Mar 2026 00:17:06 GMT  
		Size: 4.3 MB (4292146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1f507c7181795b9f9d4eb62c30721b4be08172e4c18f5affd0c50448d97dd`  
		Last Modified: Fri, 20 Mar 2026 00:17:06 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8255af9773134d1ef4a3fab8883941913bf1aeccc2fb2569d8bc7958da8c02c`  
		Last Modified: Fri, 20 Mar 2026 00:17:06 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5223ff6d316cf718bbc746d1b3afda5a3fbaa4424a71858b4e78cb77a0daaa1e`  
		Last Modified: Fri, 20 Mar 2026 00:17:17 GMT  
		Size: 539.9 MB (539933254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912c4640e9bfc9f6613a930b2ca34ece92e7976c8b63abfd2a7aceebf09b7696`  
		Last Modified: Fri, 20 Mar 2026 00:17:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8484d992ab7c3b48cbfcfb052079c79d0aa0f1bd41c8dcc684357324092029eb`  
		Last Modified: Fri, 20 Mar 2026 00:17:08 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc89a95c70b53bc11e3c46736f5e733bd2a634b71280ab32a1b0bc1ad20f0a4f`  
		Last Modified: Fri, 20 Mar 2026 00:17:08 GMT  
		Size: 74.1 KB (74111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dac20cf3b405736bd98b8c5755c0b1393e3c2bf518e1736908fb3c244785049`  
		Last Modified: Fri, 20 Mar 2026 00:17:09 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8ead16956e9f395b489b16938c8ee6f0aebbfab29e79b54b1b296f8a0b12c850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b08799beeee8ef649c2412380e3737d36e1d3c14ca1e2a549d35864f04cbcc4`

```dockerfile
```

-	Layers:
	-	`sha256:280589fc2b97105142e62251c883fafe18163a70afc88485380340b812053ce9`  
		Last Modified: Fri, 20 Mar 2026 00:17:06 GMT  
		Size: 2.1 MB (2098711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7c7169324972d22ab62b239637d5e332188a9a3a90cb35e9fef2b08abfbb56`  
		Last Modified: Fri, 20 Mar 2026 00:17:06 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.2`

```console
$ docker pull elasticsearch@sha256:56282e41f1d9c8dc437e4c99d132cf9f154def73b6ea8a25ac969a28c2f529c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2b49f8af45bfc0bbaec300e3c304b7d657aeaa0de210986e2cec7028428735ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716694945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b48c00f130e7324c466e9a5ccd4f24e40b17af7d5a7d44d4e2e6fce0ac10b5f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:18:00 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:18:00 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 20 Mar 2026 00:19:11 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:19:11 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 20 Mar 2026 00:19:11 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 20 Mar 2026 00:19:21 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 20 Mar 2026 00:19:21 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 20 Mar 2026 00:19:21 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:19:21 GMT
ENV SHELL=/bin/bash
# Fri, 20 Mar 2026 00:19:21 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:19:21 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 20 Mar 2026 00:19:21 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 20 Mar 2026 00:19:21 GMT
LABEL org.label-schema.build-date=2026-03-16T13:12:56.143057855Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=43a703737aab6baefa748bc7b69e4054926f2b2c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.2 org.opencontainers.image.created=2026-03-16T13:12:56.143057855Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=43a703737aab6baefa748bc7b69e4054926f2b2c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.2
# Fri, 20 Mar 2026 00:19:21 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.2 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 20 Mar 2026 00:19:22 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 20 Mar 2026 00:19:22 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:19:22 GMT
CMD ["eswrapper"]
# Fri, 20 Mar 2026 00:19:22 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880484490c60f7e217d22f655b314e0156f6a430e56322abaf6289764c83c098`  
		Last Modified: Fri, 20 Mar 2026 00:20:14 GMT  
		Size: 4.3 MB (4282170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e394c3bdd1921cf74c1062bc394834a81619e577cd148915d3dc7ad6adf39e05`  
		Last Modified: Fri, 20 Mar 2026 00:20:14 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd24ac1d2089634963eb0167aea56b3e7f89444e5cbf441a73809164d357c59`  
		Last Modified: Fri, 20 Mar 2026 00:20:14 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b722d9ddc4e27a52b0497703f5942a5aa16079489fd974e53392daf585a10`  
		Last Modified: Fri, 20 Mar 2026 00:20:27 GMT  
		Size: 672.3 MB (672291699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b3f45e2b7da6a09da8cd349e22e173e6f8a5043c9ff9cac90650d3b375b843`  
		Last Modified: Fri, 20 Mar 2026 00:20:16 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e03fa3da917b799595550dec6e685d36115823cf609a41f27e395a896ce6aa`  
		Last Modified: Fri, 20 Mar 2026 00:20:16 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57502ce405f03a81298934c843ada68cbfc0380a4d646b2440f3cc25f6efff89`  
		Last Modified: Fri, 20 Mar 2026 00:20:16 GMT  
		Size: 75.2 KB (75184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3092a642b34f23e8be9d4610b990078abe7c4e7acf99d581a3c68a50f07507a`  
		Last Modified: Fri, 20 Mar 2026 00:20:17 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9d06f3b87c9c11fa3b33dec9cc7a6641ad9c41f4c2e5d7c06912a3f45b724cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1b6f23bbbd6ad0b5a4172b06a5e163f2744e61e7aef629c4c5462fa44e01c5`

```dockerfile
```

-	Layers:
	-	`sha256:e5181380befea456e27d02608af943f599d222c6cf1da7068a5d53f06eb06648`  
		Last Modified: Fri, 20 Mar 2026 00:20:14 GMT  
		Size: 2.1 MB (2089789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:817a86302f84afcfe4d8aa054adb00f1edc3f9be268023e3a9476dbaf829d070`  
		Last Modified: Fri, 20 Mar 2026 00:20:14 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b3e68b4bd81448aad9d3211d39a30a7eb659590805e263682e48e0b400cf429d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.7 MB (560693123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5905d59130b16641f72b4a5cc5f2e9a6363ed053106f42ac4b1f00f84b1edc`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:15:31 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:15:31 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 20 Mar 2026 00:16:28 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:16:28 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 20 Mar 2026 00:16:28 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 20 Mar 2026 00:16:34 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Fri, 20 Mar 2026 00:16:34 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Fri, 20 Mar 2026 00:16:34 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:16:34 GMT
ENV SHELL=/bin/bash
# Fri, 20 Mar 2026 00:16:34 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:16:34 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 20 Mar 2026 00:16:34 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 20 Mar 2026 00:16:34 GMT
LABEL org.label-schema.build-date=2026-03-16T13:12:56.143057855Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=43a703737aab6baefa748bc7b69e4054926f2b2c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.2 org.opencontainers.image.created=2026-03-16T13:12:56.143057855Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=43a703737aab6baefa748bc7b69e4054926f2b2c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.2
# Fri, 20 Mar 2026 00:16:34 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.2 release=1 summary=Elasticsearch description=You know, for search.
# Fri, 20 Mar 2026 00:16:35 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 20 Mar 2026 00:16:35 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 00:16:35 GMT
CMD ["eswrapper"]
# Fri, 20 Mar 2026 00:16:35 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b6fce4af4bc289b2b03ced5a2b32a679642f30fb22e105b15768b937f5b932`  
		Last Modified: Fri, 20 Mar 2026 00:17:12 GMT  
		Size: 4.3 MB (4292122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d96e8e67cfd09e222a941ef4fb327634170c35c4d446bc02aba0e23d9b00d41`  
		Last Modified: Fri, 20 Mar 2026 00:17:12 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f5b94c539accbde1ff7f2b848c2031f026f693c065d2bc7b96f6913eb73941`  
		Last Modified: Fri, 20 Mar 2026 00:17:12 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50663469a68c281d649e68399001e85a96f24440300aa27c9d731ba7129c5d8`  
		Last Modified: Fri, 20 Mar 2026 00:17:23 GMT  
		Size: 518.1 MB (518107651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7aa78179a006d70d33e89ca5763e6533b23b09fcd05c65612da5fbf96fbc59`  
		Last Modified: Fri, 20 Mar 2026 00:17:13 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bc8414382d804d9720b4825e957cdf20d729d9837238ccc4c393c5cfb2f4d2`  
		Last Modified: Fri, 20 Mar 2026 00:17:13 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7403c2b3095226b9fe797524bcb0139d329e2735caf01c63c5bc846e71c39bbf`  
		Last Modified: Fri, 20 Mar 2026 00:17:13 GMT  
		Size: 74.1 KB (74101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b79874828baf7be313832496ff815e4f7c1c2f7dd0337dc521bab7116b94e`  
		Last Modified: Fri, 20 Mar 2026 00:17:14 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:deb6c70517f99eae6a18cc38f18d232c17e0aaf064fe894c2282f6cd4008c682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660a68d1b63fd3f8f7c95ed619288c560713f71bd57e0249a953b4aedb2df496`

```dockerfile
```

-	Layers:
	-	`sha256:dd4febd19fb69a84a135b6c9eada9646fde05ceac367f32c8a16ec99a9f7e615`  
		Last Modified: Fri, 20 Mar 2026 00:17:12 GMT  
		Size: 2.1 MB (2090351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30c565b98c1aa20f1e382396ccfde30c7ec6d3eff9eb1cb41bcdaa1f9d83b52`  
		Last Modified: Fri, 20 Mar 2026 00:17:12 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
