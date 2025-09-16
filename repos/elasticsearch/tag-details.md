<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.6`](#elasticsearch8186)
-	[`elasticsearch:8.19.3`](#elasticsearch8193)
-	[`elasticsearch:9.0.6`](#elasticsearch906)
-	[`elasticsearch:9.1.3`](#elasticsearch913)

## `elasticsearch:8.17.10`

```console
$ docker pull elasticsearch@sha256:13fdd468ca81f79617206311390d1e4a3fc152622532104c8aaae188ea22fab6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0a07d580f8cd0c59ba5aae4150a1ae8a961ea1bb0f4df8875d527f33ee30f6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676958603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25770b96ec32fa1b2b96dda9a04fe8ef8dee4200255df6b56bfe8b0cd9b75eba`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640ff32a54f918f74cc020f75f317b622a794ae769178b9bf55bf3250bda8e62`  
		Last Modified: Tue, 16 Sep 2025 00:56:26 GMT  
		Size: 4.5 MB (4493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26028e086680c014f5824215ec92e59ee544f545ac62fec3d9e354704dbef508`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 3.5 KB (3523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4902e8916b5631c52be14f509b3d5e1dc9f4389683a9fb4dc8f6d1094ac1198e`  
		Last Modified: Tue, 16 Sep 2025 00:57:02 GMT  
		Size: 642.4 MB (642446694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cad21a7b9fa8a6cb667eece750784d61bd1b96548cac9f9b8e80157b15c5af`  
		Last Modified: Mon, 15 Sep 2025 22:54:42 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c46cf9f99528689ca96a295ddb7807def9e4f2b65fd1bae43790e50c2950a71`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09c2bd59b36911d13bfabf6944a6323eeaee622fb9a0e03d920a0046ccde7d`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 163.9 KB (163939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70508771870a2a76f79778bc8c276b2a8d24714486412b9b6e7c1d0270c6120`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372b5524dcd9dfd49129df1249a0cff1da90f07055282b5073ecae2ab5de3c04`  
		Last Modified: Mon, 15 Sep 2025 22:54:43 GMT  
		Size: 115.5 KB (115541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:99bfc06aba908a120bbb63f41c9de27b90637c5948d10b3456f32c4107af7b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c507ddd11348d47d2ad5ff7346464031c7e9dd666d76fa948d52dba91942fbc8`

```dockerfile
```

-	Layers:
	-	`sha256:c883b0d7e3b167b8223e0f3aa4ae035dd9a96fd969895d48c36636c645ba4043`  
		Last Modified: Tue, 16 Sep 2025 00:25:21 GMT  
		Size: 3.2 MB (3164785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ac70da27c7d59eb3fb5e2d328c085a3e77839d20fafc2b06351d3ec1826c2e`  
		Last Modified: Tue, 16 Sep 2025 00:25:21 GMT  
		Size: 38.4 KB (38396 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d0cef9a4db6b00df5bab650ad8e2eaf10a7f3cde4ab9bfc37ef5a83daeb0a25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.2 MB (521164753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad62af1907e1cc63f86d7b86629660f0c3a54e8d020c2ad921ea10e8ea87191c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe38c1caf84efcb49d1c8f35c73f6664b25b6d1bbaa1a6bf1e2d94d7c5d6e2e`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 4.5 MB (4498611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13132e82d6196648e653017276aec78bc86b058006fe9047c0d6791ed5fa350`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 3.5 KB (3522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dd8de22458d573705b59cd4490eaa280bd06a3f6e7cb2ee5ba279a36044e75`  
		Last Modified: Tue, 16 Sep 2025 00:26:40 GMT  
		Size: 487.5 MB (487514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c17edb78f45ff64dd9b41bc3154f7ae543b72c56608dc03d76241869f72283c`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c2e43ecdebface168a55f3529b8a2060cc621a031dbb34affd8664fe9a0117`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a89e9a520fab115f7c8cf1fa847764c22f66046848fa81902207462cc13e13`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 160.4 KB (160367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea6d323aa852f81b18d82ce3b1bbebf23d889caa0767d72caec234c8c198ea0`  
		Last Modified: Mon, 15 Sep 2025 22:15:35 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0965346596322643c2d9f39b01c3d5123ffc28518c3ae45aca51dd9649d148`  
		Last Modified: Mon, 15 Sep 2025 22:15:36 GMT  
		Size: 115.5 KB (115541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0fdb9e199b8ad95148110e53c567ccb85cefad59bfcf747107ec1d2bff280fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933509e76845102273e0469cced77e929e90bfea794615ea2e59c28fbe9afa7e`

```dockerfile
```

-	Layers:
	-	`sha256:bf247467f5390f0b2bc3924d9efbd8a6ec6f46419806614132ad2de1c4b3131c`  
		Last Modified: Tue, 16 Sep 2025 00:25:26 GMT  
		Size: 3.2 MB (3164569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3687854c5edf99dc87d24212be108eb0f68c2a1e0b21271e4f48cfeca830d1ab`  
		Last Modified: Tue, 16 Sep 2025 00:25:26 GMT  
		Size: 38.6 KB (38599 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.6`

```console
$ docker pull elasticsearch@sha256:9b23042716b34b2fe9ac81113155f0aa36269dd3e0a5bd053c8b797e133d4c44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:fd5df380dfeafd661e8ef36b743fb15f3a6986a007ebc8850fbb47dc4650b604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.3 MB (688337964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c77aef8a3de8ec9fc24b1f34136a5d9424210e20552a9678949b58240cc88a`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 28 Aug 2025 08:37:13 GMT
ARG RELEASE
# Thu, 28 Aug 2025 08:37:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 28 Aug 2025 08:37:13 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 28 Aug 2025 08:37:13 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:13 GMT
ENV SHELL=/bin/bash
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.label-schema.build-date=2025-08-25T22:05:47.180118464Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=970b6c3ae853753ae66a12c1208c85a3c9728d92 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.6 org.opencontainers.image.created=2025-08-25T22:05:47.180118464Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=970b6c3ae853753ae66a12c1208c85a3c9728d92 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.6
# Thu, 28 Aug 2025 08:37:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 08:37:13 GMT
CMD ["eswrapper"]
# Thu, 28 Aug 2025 08:37:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deae7b3ca40579a649bcc319666292a8f910fe5ab75644edaef4ec4566c9178`  
		Last Modified: Mon, 15 Sep 2025 22:17:32 GMT  
		Size: 4.5 MB (4493722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7864eceb4a026985d04ec5b132f5ea4f190e45b6e40f25b72759086602a5db7`  
		Last Modified: Mon, 15 Sep 2025 22:17:32 GMT  
		Size: 3.5 KB (3521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cb50959606b9809189a82ef03d8b25f4d5ed4a611292599cb04c66cbb02599`  
		Last Modified: Mon, 15 Sep 2025 23:21:57 GMT  
		Size: 653.8 MB (653826122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2715181d77aa5998c5958d963413bb8d18bce5408e017a34062b15feea80c4bc`  
		Last Modified: Mon, 15 Sep 2025 22:17:32 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc87ef53d3333c14e75e3118795f47a5b6b3f8c07b9e6e295ffd0299f9e4ade8`  
		Last Modified: Mon, 15 Sep 2025 22:17:32 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2a2c3665d4e044555f1c0ac8f41ff794bf0defc3ec0ea26b6edb6f349e82c3`  
		Last Modified: Mon, 15 Sep 2025 22:17:32 GMT  
		Size: 163.9 KB (163933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0c4db6457d3c63be58195183e92d0fe8b4d0775879652bfcac25010ca3f497`  
		Last Modified: Mon, 15 Sep 2025 22:17:32 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6860835c5eb1a4b0dc7f5a81ac4a4ac3e7f084d5063e95431f1d4ded3e40ed`  
		Last Modified: Mon, 15 Sep 2025 22:17:32 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:18c144a47fab59d3e960533a3d1b2081286f5f29bf66259a54623eaf580a3b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3232779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08252e46501475f3ef8b92eaddf0a2d293f5fec44118b44adb9f91c9cc6e8ba7`

```dockerfile
```

-	Layers:
	-	`sha256:11dcd9e560f51eeb3d6ed5e5a0de4aeef3bc1251bf15910818f7587bc9614b51`  
		Last Modified: Tue, 16 Sep 2025 00:25:30 GMT  
		Size: 3.2 MB (3194390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2829ba1386ff9457a3b4ff3b606139d6b365cc2381be1f2502070f81a5d6e1`  
		Last Modified: Tue, 16 Sep 2025 00:25:31 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:7a19676952847d586725a02e8d1029f051ff9d1ac76c247ff78b4f2efa622806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530750538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c6252261e1afe9267378585e3b84f40c7689a70682f934827244b7eec9600f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 28 Aug 2025 08:37:13 GMT
ARG RELEASE
# Thu, 28 Aug 2025 08:37:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 28 Aug 2025 08:37:13 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Thu, 28 Aug 2025 08:37:13 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:13 GMT
ENV SHELL=/bin/bash
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.label-schema.build-date=2025-08-25T22:05:47.180118464Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=970b6c3ae853753ae66a12c1208c85a3c9728d92 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.6 org.opencontainers.image.created=2025-08-25T22:05:47.180118464Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=970b6c3ae853753ae66a12c1208c85a3c9728d92 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.6
# Thu, 28 Aug 2025 08:37:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 08:37:13 GMT
CMD ["eswrapper"]
# Thu, 28 Aug 2025 08:37:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8837a4794242b8a8020537caf74434b1048ce2162eb5561af2e0b6413b5953ae`  
		Last Modified: Mon, 15 Sep 2025 22:15:43 GMT  
		Size: 4.5 MB (4498785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312c46d025733e50620ee8aa389a0e9d8198ce2cf497ac2ef5add5d976b06c9c`  
		Last Modified: Mon, 15 Sep 2025 22:15:43 GMT  
		Size: 3.5 KB (3535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bb5229608601d3b8ee24988814dd167570a05a98b3d6ebe30252c8fa79b7f9`  
		Last Modified: Mon, 15 Sep 2025 22:15:38 GMT  
		Size: 497.1 MB (497099757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2177906b41d546f477954c8c3ecb23837e212ab5e523cbe60a81e6ac6822196c`  
		Last Modified: Mon, 15 Sep 2025 22:15:43 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9167d8c6e57f98aaa6bc82417fc8bbdd07995a1ae831868cd4c2296993238d5e`  
		Last Modified: Mon, 15 Sep 2025 22:15:43 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdef88e3d0eedb95b63a295255e8bd1ca67a944aa082b351525bcb7d0e757b9`  
		Last Modified: Mon, 15 Sep 2025 22:15:44 GMT  
		Size: 160.4 KB (160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28af819ba873b28cd5cc6f2030e796f864922e94f7f632130a5960a0ac36a24`  
		Last Modified: Mon, 15 Sep 2025 22:15:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52df6648c59b482782a8e037abe1fe4090cca094cb9d16c945e72eb24952bc4b`  
		Last Modified: Mon, 15 Sep 2025 22:15:43 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5f43f15bd9a0c3ef86a0dc322d902e8aecc66606fc1655b39f22ef825e32ef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3233395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d255c239516f80cf1438b2ac5a0294f1463f54ba802ead00fb0e9795fa16732`

```dockerfile
```

-	Layers:
	-	`sha256:c2b20939162a93b0da50c74003c29050642e4994271b5f80cf3985c8acf524aa`  
		Last Modified: Tue, 16 Sep 2025 00:25:36 GMT  
		Size: 3.2 MB (3194803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9ff150d26c4ee88806eac852801d18f910de2fbe951ba4a76416ca1159248e`  
		Last Modified: Tue, 16 Sep 2025 00:25:38 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.3`

```console
$ docker pull elasticsearch@sha256:d760cdd1ee9d7ce95138851283f4d546daf69713d6f826736cf0083d9d7cebf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:13eced40421da325e28d6565aa9de0d650585f0e4104221f539fcefa1210d1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.1 MB (695061156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb8b6671b2b3c5c230a4bec2d87efaae17f3edb1145123f563280bee7c81c45`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 28 Aug 2025 08:37:19 GMT
ARG RELEASE
# Thu, 28 Aug 2025 08:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 28 Aug 2025 08:37:19 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:19 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:19 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:19 GMT
ENV SHELL=/bin/bash
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.label-schema.build-date=2025-08-26T02:35:34.366492370Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1fde05a4d63448377eceb8fd3d51ce16ca3f02a9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.3 org.opencontainers.image.created=2025-08-26T02:35:34.366492370Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1fde05a4d63448377eceb8fd3d51ce16ca3f02a9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.3
# Thu, 28 Aug 2025 08:37:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["eswrapper"]
# Thu, 28 Aug 2025 08:37:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6e5bf74d14044ebd8cff6dadf66644b167edb3ca2cc5b486b34e6243fc18b7`  
		Last Modified: Mon, 15 Sep 2025 22:17:40 GMT  
		Size: 4.5 MB (4493743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c199c39e98365575a4b58ca96fcff9d2f222c0bfafcb154771072905c0527e`  
		Last Modified: Mon, 15 Sep 2025 22:17:38 GMT  
		Size: 3.5 KB (3520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab7687d37c30cdb02842a8482a9fe0d1d1d47ce0944db624081c5f51cce7196`  
		Last Modified: Tue, 16 Sep 2025 00:26:54 GMT  
		Size: 660.5 MB (660549292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52223e48984c4a991b36e707e241a3ed40cacdfda4c1bf11104459fe42e5f414`  
		Last Modified: Mon, 15 Sep 2025 22:17:38 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff15ed05c1c7fc2e815dbdf48f910143780308cf7d11711748782092960000c`  
		Last Modified: Mon, 15 Sep 2025 22:17:38 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e5200fcfc434e90b2cbca9a41a345c17a2c3c65fc027b37f5a1a0ec0c21ed4`  
		Last Modified: Mon, 15 Sep 2025 22:17:38 GMT  
		Size: 163.9 KB (163937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ff1e9d00e6c3517869cbc8f2ab491a48376504e635480da9721f58586e8d44`  
		Last Modified: Mon, 15 Sep 2025 22:17:38 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3a69d6196550362aa73fac611b4bb46c18c326b30309c3faa78ae47547960`  
		Last Modified: Mon, 15 Sep 2025 22:17:38 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:444dfc9afc0277487c84d4e7634cc5e20cd5dec1fab647732b7a38b236604a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1befb0649a3b62f917a2c6f12531f422d64b63e2b249a3ad73a27934145b37e8`

```dockerfile
```

-	Layers:
	-	`sha256:37cf8b057650da2688f304c8b14ab99928c134aeac65b8adb3718352a1bf059d`  
		Last Modified: Tue, 16 Sep 2025 00:25:39 GMT  
		Size: 3.2 MB (3215851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3242f2da1c2af6d586fc8feef8bb90c91a140d19f3ecc4ba7c78b9c2f62a25`  
		Last Modified: Tue, 16 Sep 2025 00:25:40 GMT  
		Size: 36.9 KB (36883 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:34824d432abbd90a94ab331083b5218b0bf8c65a871199b9ea113d21343b6ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.5 MB (537457647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e732d706499a065612cc66e8e70ee3242873262797d2ee62fa9063d8ec56bf61`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 28 Aug 2025 08:37:19 GMT
ARG RELEASE
# Thu, 28 Aug 2025 08:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 28 Aug 2025 08:37:19 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:19 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:19 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:19 GMT
ENV SHELL=/bin/bash
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.label-schema.build-date=2025-08-26T02:35:34.366492370Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1fde05a4d63448377eceb8fd3d51ce16ca3f02a9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.3 org.opencontainers.image.created=2025-08-26T02:35:34.366492370Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1fde05a4d63448377eceb8fd3d51ce16ca3f02a9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.3
# Thu, 28 Aug 2025 08:37:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["eswrapper"]
# Thu, 28 Aug 2025 08:37:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f917c334f4eb923d7d25648d4ab7740bf9116c740beb1536c140b3adc9d7ac2`  
		Last Modified: Mon, 15 Sep 2025 22:15:41 GMT  
		Size: 4.5 MB (4498691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea77bdd320869ee3acbaffdebb4adf88c100bcf033af2023ab27733b0cb4d22`  
		Last Modified: Mon, 15 Sep 2025 22:15:40 GMT  
		Size: 3.5 KB (3530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5022f7c0f1c80288c2b7b34b096ce86fa43a9c12180a0c0147343e76255738f5`  
		Last Modified: Mon, 15 Sep 2025 23:20:51 GMT  
		Size: 503.8 MB (503806958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01bf11da6faa470d682c1181d5143b39d051ca63b30195bc3134d1966cd908`  
		Last Modified: Mon, 15 Sep 2025 22:15:40 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d36fe576e9ee2d439e6d012d6ffca9d2932d3083d84a4143d60886f811fa525`  
		Last Modified: Mon, 15 Sep 2025 22:15:40 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ed0dc8bd577bc3d3ae20a0d1582a829d709c82ab3e7e49da645bf5c1a415b3`  
		Last Modified: Mon, 15 Sep 2025 22:15:40 GMT  
		Size: 160.4 KB (160365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c04043f7c9ecd97857a28ae51ce0541b7c7c03e4e6d63b0f79ec4b1af7c178`  
		Last Modified: Mon, 15 Sep 2025 22:15:40 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea29446041a204615056754eab7ab574c42a22e5964732d42a2450d4170fede`  
		Last Modified: Mon, 15 Sep 2025 22:15:40 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:07f4e6de997470acef359c3179002b6a1f51c961d460cd97adecd399a5b05953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f03b5f3e9591b9e687638058990b97c79a3775aed4f83a6e8767b65ecf6039`

```dockerfile
```

-	Layers:
	-	`sha256:cb7f28015ca75bcc76f38023e2073433e0afcfbe7c874ec3f47dc86abb481f91`  
		Last Modified: Tue, 16 Sep 2025 00:25:45 GMT  
		Size: 3.2 MB (3216264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11cb721881ea5321380a7efdcb95b27a9373ca71ac3caae87561d86f38d70707`  
		Last Modified: Tue, 16 Sep 2025 00:25:46 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.6`

```console
$ docker pull elasticsearch@sha256:8c966f6b7e8c2b646b2aca339263ea019dd53408fe3dc4371e7550c27336a6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0e9d62c371d89dc839a3b3c615063544a1b967e89b6dff21d3e05186307986bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700375639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f10a565d6b7456a0c01710cdd56555baf82af26a9d01300b4f551a9144c1c7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:14:25 GMT
ENV container oci
# Wed, 20 Aug 2025 13:14:25 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:14:26 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:20 GMT
ENV SHELL=/bin/bash
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL org.label-schema.build-date=2025-08-24T22:05:07.219522691Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c519c0e3cfc2464e0eb0c09996b683e40b4235cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.6 org.opencontainers.image.created=2025-08-24T22:05:07.219522691Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c519c0e3cfc2464e0eb0c09996b683e40b4235cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.6
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Sep 2025 11:31:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Sep 2025 11:31:20 GMT
CMD ["eswrapper"]
# Tue, 02 Sep 2025 11:31:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d46736b3e58617d122395d8f3624f6f60a386aba11eb4a3534c9c5969bfae3`  
		Last Modified: Tue, 02 Sep 2025 17:27:47 GMT  
		Size: 4.3 MB (4284033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ccd3df6c185ae86c9b0fc7e31664f62dd6d34e7e4e3334c2c257105fb3a944`  
		Last Modified: Tue, 02 Sep 2025 17:27:47 GMT  
		Size: 1.5 KB (1533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8301d5428865fe5f4a9e423864cde550f44a31754791e252f1f3ae15cbbc3717`  
		Last Modified: Tue, 02 Sep 2025 17:27:47 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f2b208405214a1b97165d0cd32f811e47477c77f9fcc460a83cdd7bd0601c3`  
		Last Modified: Tue, 02 Sep 2025 18:33:00 GMT  
		Size: 656.4 MB (656353796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f170040cd179e0074d6bf64211dd609ad2479055485fb3148d6fb7e712b9ab8e`  
		Last Modified: Tue, 02 Sep 2025 17:27:47 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7273961c01ba13cdad616af13011a5eb7024e4d44a4e8d68a7a0f2d85c7da8`  
		Last Modified: Tue, 02 Sep 2025 17:27:48 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73cac8be0e12defb736d722cda585b9cb860df583877a69c0f564f1abafa32c`  
		Last Modified: Tue, 02 Sep 2025 17:27:48 GMT  
		Size: 75.7 KB (75742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0030095da2b3a5a91ea1591ebf756a6c62b86e11631c522e2a78423c09c49295`  
		Last Modified: Tue, 02 Sep 2025 17:27:48 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a89056473b84c35c7be13003933515fc65a4c9fd55df15fe621afe1df2680508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d15dc968b1221a71c861fc28a02c2d80dd2eeee2b26ebc671102563e2fd779f`

```dockerfile
```

-	Layers:
	-	`sha256:9eee949ca729638280384e458561f4247c66efed100dee02447b6e19071efb71`  
		Last Modified: Tue, 02 Sep 2025 18:25:39 GMT  
		Size: 2.0 MB (2030699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0125f6ebc36f3d5e5b24cbf9d6a3cc5860d8e20cae597b3d017ee43e0ed661ed`  
		Last Modified: Tue, 02 Sep 2025 18:25:40 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:839fcba3e2d5e13eeb3b355003a93823987285b30515b239cb804d8169eb123c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.9 MB (538858729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae411ab7b89364f2f95c07829d8301ba907d5807c98f578b901660506b2b8b2c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:15:03 GMT
ENV container oci
# Wed, 20 Aug 2025 13:15:04 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:15:04 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:20 GMT
ENV SHELL=/bin/bash
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL org.label-schema.build-date=2025-08-24T22:05:07.219522691Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c519c0e3cfc2464e0eb0c09996b683e40b4235cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.6 org.opencontainers.image.created=2025-08-24T22:05:07.219522691Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c519c0e3cfc2464e0eb0c09996b683e40b4235cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.6
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Sep 2025 11:31:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Sep 2025 11:31:20 GMT
CMD ["eswrapper"]
# Tue, 02 Sep 2025 11:31:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6cfb60ffc9315a7fd95e258b3d01246ce21f14bb090c028e75c366fb7b4b2f`  
		Last Modified: Tue, 02 Sep 2025 17:41:47 GMT  
		Size: 4.3 MB (4293014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81385e4903430b053f077f100e40110ff1c9b830f526f5fd39f58841d2dac29`  
		Last Modified: Tue, 02 Sep 2025 17:41:50 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ab5703ca385b2f0da76e0dd71463d310b61d145e5f0bc29c2a8d479a8b16d6`  
		Last Modified: Tue, 02 Sep 2025 17:41:50 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64994d71f229bafc908a81be757f2d3eafb9a7c6139afb8141c6b1171ccc6278`  
		Last Modified: Tue, 02 Sep 2025 18:34:08 GMT  
		Size: 496.6 MB (496617157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8864b7a6faec871870be8af4a76df45e1d23fdeb1acd60ef8554e629be15ae8`  
		Last Modified: Tue, 02 Sep 2025 17:41:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ae2e2dcb02eedf494e14188dddf7e5605079555734571e9eafec448ee1578`  
		Last Modified: Tue, 02 Sep 2025 17:41:51 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4d3d95b187bd488511682f1bf72104a8e339197741ad3831b4acc6447cae6`  
		Last Modified: Tue, 02 Sep 2025 17:41:52 GMT  
		Size: 74.6 KB (74634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b3ad77e79de4aa3de442ca63ad5cf8bb82673770edb9d7b5d546afc009c59b`  
		Last Modified: Tue, 02 Sep 2025 17:41:52 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:20164798083e83ab2c37e9c06cecd2e6bec042f4be74bb94ef68756ed1094c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5b1918884bbe94694d135aff62033646c59ea3c37e1db519f5fd0df7b6170d`

```dockerfile
```

-	Layers:
	-	`sha256:642499e6dedc2ecc643d49b192c1ec0e4053944a45fafc68c2df62db78398560`  
		Last Modified: Tue, 02 Sep 2025 18:25:45 GMT  
		Size: 2.0 MB (2031263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7cf3c58c94ec9e600000aee5b120f31326fa196c4f6255e05b52fe4f708dd1`  
		Last Modified: Tue, 02 Sep 2025 18:25:46 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.3`

```console
$ docker pull elasticsearch@sha256:05069ffdf546dbb8d1e3f1b9fcf0d8d7e9aa9164d4b85153936e356a4173aba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6177bc87b6ea5e0d63c872707080699feaf6edac41c7f4cca04c7677bce36f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.2 MB (715231610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6895cd1669fe448ee82e6ed45791ce2c24ab0f2088f3b34040edc0ec90d3c216`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:14:25 GMT
ENV container oci
# Wed, 20 Aug 2025 13:14:25 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:14:26 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:33 GMT
ENV SHELL=/bin/bash
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL org.label-schema.build-date=2025-08-24T22:05:04.526302670Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0c781091a2f57de895a73a1391ff8426c0153c8d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.3 org.opencontainers.image.created=2025-08-24T22:05:04.526302670Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0c781091a2f57de895a73a1391ff8426c0153c8d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.3
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Sep 2025 11:31:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Sep 2025 11:31:33 GMT
CMD ["eswrapper"]
# Tue, 02 Sep 2025 11:31:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934d714799cb80a828c44d158d5f12e8d6f94b696fa1cdce3a1d36d389bb2f74`  
		Last Modified: Tue, 02 Sep 2025 17:27:59 GMT  
		Size: 4.3 MB (4283952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8444b85a0601e8d51456a957e6adbedc16081a7b215083c8909bdbe38e172a`  
		Last Modified: Tue, 02 Sep 2025 17:27:58 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9bcecba2266577b8bcc570b90a72f17d78bc155909d1ae7dae5104b380e45f`  
		Last Modified: Tue, 02 Sep 2025 17:27:58 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32c6c73a671c7e6c01cac0be9471cb573724e615467d9648ac66039748958b6`  
		Last Modified: Tue, 02 Sep 2025 18:29:17 GMT  
		Size: 671.2 MB (671209844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a10648d3eed4cece6e8ec49b3e1b56ab9c289588a73a6b5dcaf0f8b930d12b`  
		Last Modified: Tue, 02 Sep 2025 17:27:58 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb93096ef8e76ce06f4511374a4d27e1e57d0cde23b29e6c841f002a07a31d8`  
		Last Modified: Tue, 02 Sep 2025 17:27:59 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b4ee2f76d34b136891bde98bb80fb34bd95860928d33be648bf8e9fccb5037`  
		Last Modified: Tue, 02 Sep 2025 17:27:59 GMT  
		Size: 75.7 KB (75745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d5cd140d2a30379e02f13190b772e9e6756da848708d3720c07f537736ea20`  
		Last Modified: Tue, 02 Sep 2025 17:27:58 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ee599de1b09bd7cf00f883e883f1972e9594cf4bc03119740df1b6d4993f5f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a918d3edb0822af3b32034752d4f7672da9b763f4dd2933bb7f7c11fea8969c3`

```dockerfile
```

-	Layers:
	-	`sha256:d5aacb34a19c936aeaac5d23d8e6c9470302842c09c51642e51f51ee702da1ab`  
		Last Modified: Tue, 02 Sep 2025 18:25:50 GMT  
		Size: 2.1 MB (2085058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5debb9c28c2675693b2fa55886c9920c5b089fcaa79dfa94b769d4559f7b0183`  
		Last Modified: Tue, 02 Sep 2025 18:25:52 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:9a497f5637477f0f3d34419e602023a3aed1d8be9db8638092963b1b919b302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553705656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02e88a1e9a725987a8aa7d62108f39867d28cc411147936fd8ca5eab5275107`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:15:03 GMT
ENV container oci
# Wed, 20 Aug 2025 13:15:04 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:15:04 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:33 GMT
ENV SHELL=/bin/bash
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL org.label-schema.build-date=2025-08-24T22:05:04.526302670Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0c781091a2f57de895a73a1391ff8426c0153c8d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.3 org.opencontainers.image.created=2025-08-24T22:05:04.526302670Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0c781091a2f57de895a73a1391ff8426c0153c8d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.3
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Sep 2025 11:31:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Sep 2025 11:31:33 GMT
CMD ["eswrapper"]
# Tue, 02 Sep 2025 11:31:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6cfb60ffc9315a7fd95e258b3d01246ce21f14bb090c028e75c366fb7b4b2f`  
		Last Modified: Tue, 02 Sep 2025 17:41:47 GMT  
		Size: 4.3 MB (4293014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81385e4903430b053f077f100e40110ff1c9b830f526f5fd39f58841d2dac29`  
		Last Modified: Tue, 02 Sep 2025 17:41:50 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ab5703ca385b2f0da76e0dd71463d310b61d145e5f0bc29c2a8d479a8b16d6`  
		Last Modified: Tue, 02 Sep 2025 17:41:50 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62999c8aeab0e608f469daffec1b6b3094a94b1699e32f8c32c647276310b9c`  
		Last Modified: Tue, 02 Sep 2025 18:33:33 GMT  
		Size: 511.5 MB (511464078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d208372b1b8ebfd845e5797227be62b51e760933411409562fbd42404b1a9675`  
		Last Modified: Tue, 02 Sep 2025 17:43:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8235ff51b49b0b3abdcff1eb3db303ba2461385342ec449f162d51657dc9f8c4`  
		Last Modified: Tue, 02 Sep 2025 17:43:51 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e058de940a26a581fb5953162ca5b3a724f7d143facd7ec125af8cf1a965674`  
		Last Modified: Tue, 02 Sep 2025 17:43:51 GMT  
		Size: 74.6 KB (74639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84979c2afd670a0b04441a98402f4ccd1292e567a526e9ebbdc457acc999f38`  
		Last Modified: Tue, 02 Sep 2025 17:43:52 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:917f03333a8b3e0eac59737dad483fe3bc94996d3e6605553801f09646688668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf30c206aa8531aac99452724008a689eae75f51a1a171e2324c2e8e91bb58e`

```dockerfile
```

-	Layers:
	-	`sha256:739ed8b2789cc736592f591447fcb2607821bbfa5726173291adfc4f4a3ffdd3`  
		Last Modified: Tue, 02 Sep 2025 18:25:56 GMT  
		Size: 2.1 MB (2085622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40682fb5517826b7eb3f3182e71a8a397fd49b5f1cbcd768cf1775955ef53c39`  
		Last Modified: Tue, 02 Sep 2025 18:25:57 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
