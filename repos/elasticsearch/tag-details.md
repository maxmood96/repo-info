<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.12`](#elasticsearch81912)
-	[`elasticsearch:9.2.6`](#elasticsearch926)
-	[`elasticsearch:9.3.1`](#elasticsearch931)

## `elasticsearch:8.19.12`

```console
$ docker pull elasticsearch@sha256:7f68ead6c5415a1ca4b333c8e131c914a7201b8859a6d2b010205f07e82e714e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.12` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2f2dd201c3eb5d70f310bdb7bcfb2ff9d115371daedf2beffa1ea7992a9771ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.8 MB (716839951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2be6f08690e3c1abee099abed8b301f0104a2983676af51df56b2151b77ca0`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 26 Feb 2026 19:29:46 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 26 Feb 2026 19:29:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 26 Feb 2026 19:29:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:29:47 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Feb 2026 19:36:03 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 26 Feb 2026 19:36:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:36:03 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:36:03 GMT
ENV SHELL=/bin/bash
# Thu, 26 Feb 2026 19:36:03 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Feb 2026 19:36:04 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 26 Feb 2026 19:36:04 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 26 Feb 2026 19:36:04 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 26 Feb 2026 19:36:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 26 Feb 2026 19:36:04 GMT
LABEL org.label-schema.build-date=2026-02-23T23:08:40.713020893Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=840cd2a58b052d1632219ee0b8dcc0f364226287 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.12 org.opencontainers.image.created=2026-02-23T23:08:40.713020893Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=840cd2a58b052d1632219ee0b8dcc0f364226287 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.12
# Thu, 26 Feb 2026 19:36:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:36:04 GMT
CMD ["eswrapper"]
# Thu, 26 Feb 2026 19:36:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d49ae9f7f4982b4e5682486c2f1e2c5a9e27146be310f4a50ae0bc42c524ee`  
		Last Modified: Thu, 26 Feb 2026 19:36:55 GMT  
		Size: 6.6 MB (6617894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11343baa9cd2ee9c1cfba73d53f30f43c1afe818e3266995b5cb5f4417b08e9c`  
		Last Modified: Thu, 26 Feb 2026 19:36:54 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc35d3eb3969d04be587d0845eed87e697a4e8b0f625c5a4019d37358c55bb4`  
		Last Modified: Thu, 26 Feb 2026 19:37:09 GMT  
		Size: 680.2 MB (680199761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5a7a09eca4552c8eebe09d6a2634746a3509c97e7804e6b2bd46a3e32cec3b`  
		Last Modified: Thu, 26 Feb 2026 19:36:54 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a2c63f11991b0006e45a45c5d693b33470fca0e2a4cf9dc62c1be2b75edd14`  
		Last Modified: Thu, 26 Feb 2026 19:36:56 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c969d40bf261599e7dcdb0429c91dee0e51eba3198b37b22ff62fb84789547a1`  
		Last Modified: Thu, 26 Feb 2026 19:36:56 GMT  
		Size: 163.9 KB (163938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a753ec3d40190cd386d0beab407470f9bf262ba53e3ad5dfc74c3b15c97aa30`  
		Last Modified: Thu, 26 Feb 2026 19:36:56 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dc280cf7a05b1e07b0c68a96ba29e72f2653adc2fd085f0ab40a052a3946c0`  
		Last Modified: Thu, 26 Feb 2026 19:36:57 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.12` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0fec7135ab70dba65deaec8082da609814274921057e0c4ef57800ae48a73428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1e3811af18f4af12a40f9c3455372fece0cc6743aad1cad979783dcdd9ffa0`

```dockerfile
```

-	Layers:
	-	`sha256:256fff491ec1f78d75c8855467b7d02dddb228999b26f028478ef869b366b8aa`  
		Last Modified: Thu, 26 Feb 2026 19:36:54 GMT  
		Size: 3.2 MB (3208984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe17ea2965d03b832179c7366c55b667f501f8cc83d7341149a6691670e1ddf`  
		Last Modified: Thu, 26 Feb 2026 19:36:54 GMT  
		Size: 36.8 KB (36847 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.12` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:01d2934b22d701abfcfd6d0efe667a9b315230b5dfbcd8d9431aab9d7601888e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.6 MB (564601963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547362620b18ef35da1acc460fe343b663f4218e189debcfb6351d392df6d226`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Feb 2026 19:01:56 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 26 Feb 2026 19:01:56 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 26 Feb 2026 19:01:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:01:56 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Feb 2026 19:02:40 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 26 Feb 2026 19:02:40 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:02:40 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:02:40 GMT
ENV SHELL=/bin/bash
# Thu, 26 Feb 2026 19:02:40 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Feb 2026 19:02:41 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 26 Feb 2026 19:02:41 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 26 Feb 2026 19:02:41 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 26 Feb 2026 19:02:41 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 26 Feb 2026 19:02:41 GMT
LABEL org.label-schema.build-date=2026-02-23T23:08:40.713020893Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=840cd2a58b052d1632219ee0b8dcc0f364226287 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.12 org.opencontainers.image.created=2026-02-23T23:08:40.713020893Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=840cd2a58b052d1632219ee0b8dcc0f364226287 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.12
# Thu, 26 Feb 2026 19:02:41 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:02:41 GMT
CMD ["eswrapper"]
# Thu, 26 Feb 2026 19:02:41 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4f5853aa0f40031d35eb39c1f3203c639fb18681e38b5a8d654790497f797e`  
		Last Modified: Thu, 26 Feb 2026 19:03:21 GMT  
		Size: 6.5 MB (6516238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcfe90a9aa795720d4850f4544e8864a86ab9999fde6296ce0fbac01733f319`  
		Last Modified: Thu, 26 Feb 2026 19:03:20 GMT  
		Size: 3.5 KB (3530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da116bf102894b6cfd443364529724bd3222d205f7ea678917bbb6f9354018f`  
		Last Modified: Thu, 26 Feb 2026 19:03:30 GMT  
		Size: 528.9 MB (528929906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1182df4efd5fc880925f8492f142c74105990a20c6f92df4cb9fe50b09c5f7`  
		Last Modified: Thu, 26 Feb 2026 19:03:20 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cc513ba436fd91e8c49226af1f7252167753e8cab8e724197ca8f0edf65ed8`  
		Last Modified: Thu, 26 Feb 2026 19:03:22 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae62f964a7cac6292838584992ae95695e50d86623ab485ab991e32e194c01a`  
		Last Modified: Thu, 26 Feb 2026 19:03:22 GMT  
		Size: 160.4 KB (160372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9984995a2d6043b00898c75512b8094561eaf9f01032df4eb0d152c05fbb62f`  
		Last Modified: Thu, 26 Feb 2026 19:03:22 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7caad328151a0b12f19e930064ed2dfce88b57231064103baf274e5f8de92`  
		Last Modified: Thu, 26 Feb 2026 19:03:23 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.12` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0fce97c380406d52af0924e51b7b3839f1d87c718cc35122504cbd54fa60b414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cfb874b0bb5ce3c9f59e921e428866af672315a24157595e17001aedd07b2f`

```dockerfile
```

-	Layers:
	-	`sha256:39927071cd314b687a6b515f1fc3894a9c74581490a0d81bfd42c2e57be05074`  
		Last Modified: Thu, 26 Feb 2026 19:03:21 GMT  
		Size: 3.2 MB (3209397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe324fa8965ca6342e2f46b700f3e8cdf192b8f7481d46b990c0522946deb463`  
		Last Modified: Thu, 26 Feb 2026 19:03:20 GMT  
		Size: 37.0 KB (37049 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.6`

```console
$ docker pull elasticsearch@sha256:75689dc3f07e725ee6d1a35255ddaa0232f90d447ebecd11537e60aa7e8b809d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b49f8c95ad0f0b1013cdc20c67d2a16ec317587d0099e0e967a9dcade2704b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.5 MB (738464548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fe1338f16bc1a0d4ef711881cbbd67162e36441ee6a4721b5f602a863d8c46`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Thu, 26 Feb 2026 19:02:01 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:02:01 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 26 Feb 2026 19:02:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:02:44 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:02:44 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Feb 2026 19:02:54 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 26 Feb 2026 19:02:54 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 26 Feb 2026 19:02:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:02:54 GMT
ENV SHELL=/bin/bash
# Thu, 26 Feb 2026 19:02:54 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Feb 2026 19:02:54 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 26 Feb 2026 19:02:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 26 Feb 2026 19:02:54 GMT
LABEL org.label-schema.build-date=2026-02-23T23:37:17.026418401Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b6e59ddaac5fc0c537d10132b2a1d5511ff8b1b5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-23T23:37:17.026418401Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b6e59ddaac5fc0c537d10132b2a1d5511ff8b1b5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6
# Thu, 26 Feb 2026 19:02:54 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.6 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 26 Feb 2026 19:02:54 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 26 Feb 2026 19:02:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:02:54 GMT
CMD ["eswrapper"]
# Thu, 26 Feb 2026 19:02:54 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551a822ffea0d8e3e30f7ad6950de645928d73085ce4e5bd7a5299855032be1c`  
		Last Modified: Thu, 26 Feb 2026 19:03:47 GMT  
		Size: 4.3 MB (4282806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386bf2a7c4d8e240c8e8a0708c543646c43a0124a03c3cf5c046c8f035a34546`  
		Last Modified: Thu, 26 Feb 2026 19:03:47 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63196d49671f1a4fe2b60973eb32ba50f677553fdbb2b85bcb928869a03e052d`  
		Last Modified: Thu, 26 Feb 2026 19:03:47 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a72f6035036fdda7cbbfbb44cd5d79ef241c58e8e7a1549b4bb0c1925ba4a63`  
		Last Modified: Thu, 26 Feb 2026 19:04:00 GMT  
		Size: 694.1 MB (694058187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dbd2a2b616857a1a18e74b9a651b7e3a098812e9c5cb7aafa40bfe8e21c554`  
		Last Modified: Thu, 26 Feb 2026 19:03:48 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5837a6933bc8c47eaff7af3e8d936112b96b73b1b7d031e8c4bc7f250bb2a8a6`  
		Last Modified: Thu, 26 Feb 2026 19:03:48 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf49a51e81ed4cd760ae95f53415b648ac49e4d06db67e4b3b0024484886a81`  
		Last Modified: Thu, 26 Feb 2026 19:03:48 GMT  
		Size: 75.2 KB (75180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5ae4765fb3505c29cb6eef9fdf5852b798cdd1090a410de2426875cb85e5ed`  
		Last Modified: Thu, 26 Feb 2026 19:03:49 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:69d13e3d5bd97d1ed0771ef7ab18008d81433d1ad844d0a8f86d3ef782079486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac432feb89f0aef9096ddc3a8eabb0f46aa2c0e69e7eedee3cbfa9bc656abbb9`

```dockerfile
```

-	Layers:
	-	`sha256:0b6d2f4d9bbcdde40b7e71011aeb61b7245e102bcf0e861880116d0e000741e6`  
		Last Modified: Thu, 26 Feb 2026 19:03:47 GMT  
		Size: 2.1 MB (2098143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197fc5ca783966992e355619ecdb7de0d69b612c0b76fb4156c671ef4f6ac08a`  
		Last Modified: Thu, 26 Feb 2026 19:03:47 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d493adeed5834ef38fc30681b3fc947c3892be66c497d2a3c536a7f246a0702f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.5 MB (582475229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774c528db425461c472ed4de4cd8bd9187ec6162b207292ef750b6252c5a97e6`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Thu, 26 Feb 2026 19:02:11 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:02:11 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 26 Feb 2026 19:02:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:02:46 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:02:46 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Feb 2026 19:02:53 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 26 Feb 2026 19:02:53 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 26 Feb 2026 19:02:53 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:02:53 GMT
ENV SHELL=/bin/bash
# Thu, 26 Feb 2026 19:02:53 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Feb 2026 19:02:53 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 26 Feb 2026 19:02:53 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 26 Feb 2026 19:02:53 GMT
LABEL org.label-schema.build-date=2026-02-23T23:37:17.026418401Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b6e59ddaac5fc0c537d10132b2a1d5511ff8b1b5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-23T23:37:17.026418401Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b6e59ddaac5fc0c537d10132b2a1d5511ff8b1b5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6
# Thu, 26 Feb 2026 19:02:53 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.6 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 26 Feb 2026 19:02:53 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 26 Feb 2026 19:02:53 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:02:53 GMT
CMD ["eswrapper"]
# Thu, 26 Feb 2026 19:02:53 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b208af194b32725394b02ff928b4d4c1e7f03c8e532f0ce0c2217568fad26`  
		Last Modified: Thu, 26 Feb 2026 19:03:33 GMT  
		Size: 4.3 MB (4289706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5015da519fb036688c10f5672cc7525a45e15ac677b4bdfac8cb1fda004e067`  
		Last Modified: Thu, 26 Feb 2026 19:03:33 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596d4a2a65ee4971e7fe6e9ce1ae9eb2d1fa2795bd8f1d2d235299c895a57148`  
		Last Modified: Thu, 26 Feb 2026 19:03:33 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9aa6a278fd6ad9c885e9486b43e719355a8a83c9d093694d7a08bad89f112e`  
		Last Modified: Thu, 26 Feb 2026 19:03:57 GMT  
		Size: 539.9 MB (539894527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ee8d58fc747a596467ccd3a258a68a7a8a07a46ec45289c520e4a12239bd1e`  
		Last Modified: Thu, 26 Feb 2026 19:03:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f54e5ff4b7a01d7534c02e96f7ac18f22360b44e12f5cb6adda8b577ce8c6e4`  
		Last Modified: Thu, 26 Feb 2026 19:03:34 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f045835e304f6e0b19ea366467fe7b66f4e01004fca69d0e9b1d4b6b28bb0c4c`  
		Last Modified: Thu, 26 Feb 2026 19:03:34 GMT  
		Size: 74.1 KB (74111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b37230adeec6b3b876cfeae68fa8e61af78163cdecbcd05cca893c5e9a94602`  
		Last Modified: Thu, 26 Feb 2026 19:03:35 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6a135efbdd7288c099d58ffee59af36250556a7c05e4415ba799382e15015afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e8069c8c6d024e349d7dab4348a77677577de7b97a7c5fed8b75cbc627a60b`

```dockerfile
```

-	Layers:
	-	`sha256:e108445390313773ff8817e5a6945a10b90274159ab3dca25dc225b2686655fa`  
		Last Modified: Thu, 26 Feb 2026 19:03:33 GMT  
		Size: 2.1 MB (2098705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ada9dbbd0c7233a12edd0ef3fc01c7693bfb75400a9e07d7a5478ddd7f38f7`  
		Last Modified: Thu, 26 Feb 2026 19:03:33 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.1`

```console
$ docker pull elasticsearch@sha256:2cc6bb7210e693c9ee96a2d37833dbd8d3edaacfc0e468d9daa04cb7a125e9a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9ac430f43e65d74a63b9d3a02c1e57253e3f0717baff3a2238830cf17116265b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.6 MB (716638970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7655101440df59fa78a069422f8e58f7ade90c253e59c63916a34716f32d37d`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Thu, 26 Feb 2026 19:02:40 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:02:40 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 26 Feb 2026 19:03:23 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:03:23 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:03:23 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Feb 2026 19:03:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 26 Feb 2026 19:03:33 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 26 Feb 2026 19:03:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:03:33 GMT
ENV SHELL=/bin/bash
# Thu, 26 Feb 2026 19:03:33 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Feb 2026 19:03:33 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 26 Feb 2026 19:03:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 26 Feb 2026 19:03:33 GMT
LABEL org.label-schema.build-date=2026-02-23T23:37:38.684779921Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0dd66e52ba3aa076cf498264e46339dbb71f0269 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-23T23:37:38.684779921Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0dd66e52ba3aa076cf498264e46339dbb71f0269 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1
# Thu, 26 Feb 2026 19:03:33 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.1 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 26 Feb 2026 19:03:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 26 Feb 2026 19:03:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:03:33 GMT
CMD ["eswrapper"]
# Thu, 26 Feb 2026 19:03:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efbb8ef1e3d74552c18b4e0b596e041951542d805cc9ce579f5db3bacdcd46`  
		Last Modified: Thu, 26 Feb 2026 19:04:23 GMT  
		Size: 4.3 MB (4282732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59952b31672480fd7147f4e29e72b01feb8e18521a126e4adcbfc297883595d6`  
		Last Modified: Thu, 26 Feb 2026 19:04:23 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265840e888e6fb4f52b47bd207eaa124977956ff65b8be59d3c8e4d31fa6766b`  
		Last Modified: Thu, 26 Feb 2026 19:04:23 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb6b6fe489fbeb970a477b90c494a60f830025cb13bf0f859bbd55349b2a12`  
		Last Modified: Thu, 26 Feb 2026 19:04:42 GMT  
		Size: 672.2 MB (672232683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd42d93ade1f49545fad0c5952ab87c6879ecb898e373e38bb24c9cfb338616`  
		Last Modified: Thu, 26 Feb 2026 19:04:24 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e23326880df6e625ec795ee9cb629fe92864c88c3b1e9408a797205acb8654`  
		Last Modified: Thu, 26 Feb 2026 19:04:24 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd47902fd2aae731716aeb00adc9b3ea4114cef98694f2e2eb32a5792676fd7e`  
		Last Modified: Thu, 26 Feb 2026 19:04:24 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ecd5d5fa70b30e8be855a3a8d8ee332381d4fda1e384fb43a427115fae068`  
		Last Modified: Thu, 26 Feb 2026 19:04:25 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:962eb5e44e0119544dd29af48fd887be593fb3b97f3f34a7b75924225ff62c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7899401c60ad4a19bb494221503b711ef6149d5b2fcce05d7e3c258c6d4a75`

```dockerfile
```

-	Layers:
	-	`sha256:303210106a13deb4c448066df31e4b2a85282a14c8ca8bafc8f5f1dd61985ded`  
		Last Modified: Thu, 26 Feb 2026 19:04:23 GMT  
		Size: 2.1 MB (2089783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a337a140a66c84f7fdbd99440503c5a3c6ba6701ac9903fae7277e229b556`  
		Last Modified: Thu, 26 Feb 2026 19:04:23 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:b1e9205b3789b6f3984dd077e3ca14d43a65c5aba5e64f89e92421f72ae1b1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560628940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69d30afcd65852859dc520e1b4d5df6c9f79a3bf72da515e2bf792ac52204cc`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Thu, 26 Feb 2026 19:02:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:02:21 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 26 Feb 2026 19:12:00 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:12:00 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:12:00 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Feb 2026 19:12:06 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 26 Feb 2026 19:12:07 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 26 Feb 2026 19:12:07 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:12:07 GMT
ENV SHELL=/bin/bash
# Thu, 26 Feb 2026 19:12:07 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Feb 2026 19:12:07 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 26 Feb 2026 19:12:07 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 26 Feb 2026 19:12:07 GMT
LABEL org.label-schema.build-date=2026-02-23T23:37:38.684779921Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0dd66e52ba3aa076cf498264e46339dbb71f0269 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-23T23:37:38.684779921Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0dd66e52ba3aa076cf498264e46339dbb71f0269 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1
# Thu, 26 Feb 2026 19:12:07 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.1 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 26 Feb 2026 19:12:07 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 26 Feb 2026 19:12:07 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:12:07 GMT
CMD ["eswrapper"]
# Thu, 26 Feb 2026 19:12:07 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a390beeb39d0f8bc422fb8ba234114f9d0f6a2646bf409294e3e5f046e687d6`  
		Last Modified: Thu, 26 Feb 2026 19:12:45 GMT  
		Size: 4.3 MB (4289716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93103cacf670888ce67921737c83b8bde4105a1b31ef8c819a1e84e00b6530f`  
		Last Modified: Thu, 26 Feb 2026 19:12:45 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1512a2f3cc234f6695fbffa2ba3f632b79a9ad3817b2d1822d2b3521a90764b3`  
		Last Modified: Thu, 26 Feb 2026 19:12:45 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ce4c9d3c4b8b1684fc802ab2bfe800bb5e25fc096a7791a174d6d2530f6dc3`  
		Last Modified: Thu, 26 Feb 2026 19:12:54 GMT  
		Size: 518.0 MB (518048241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908b221c4edcca9248b3b553a5edcddc1bdfb47f7dd5595acdaee0305b82e7b2`  
		Last Modified: Thu, 26 Feb 2026 19:12:46 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e38320301f8b617391cf7117fc58d072e87c4bb6213ee9535eb35cc7e9b52b`  
		Last Modified: Thu, 26 Feb 2026 19:12:46 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ec29d5529a353f176deee38e8514537aa037546f97017145834b6b32d45610`  
		Last Modified: Thu, 26 Feb 2026 19:12:46 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f2c046ee77560acdf5ff6ffc5dfa899bda7e7961363f885ebb259d361c0e73`  
		Last Modified: Thu, 26 Feb 2026 19:12:47 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:89947f8bb72e17e3b23ece8125ab9996440c03618cd125b2c9ca68820d0473cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31109d2e5f480977ec7fdeb7370888e0dcf9fe8ef4375a0d2bf3aab731ed086a`

```dockerfile
```

-	Layers:
	-	`sha256:03042a9991509cb6cdd55ab3ec08442d868fda95be22ef1c87f0bb8f57067063`  
		Last Modified: Thu, 26 Feb 2026 19:12:45 GMT  
		Size: 2.1 MB (2090345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76fe40eb06b960b8aa674b2b49df0005f5c03a6e5d1c2eec6a2d1c049630140a`  
		Last Modified: Thu, 26 Feb 2026 19:12:45 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
