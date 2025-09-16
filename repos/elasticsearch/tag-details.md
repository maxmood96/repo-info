<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.7`](#elasticsearch8187)
-	[`elasticsearch:8.19.3`](#elasticsearch8193)
-	[`elasticsearch:9.0.7`](#elasticsearch907)
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

## `elasticsearch:8.18.7`

```console
$ docker pull elasticsearch@sha256:37e851eb4e9b5961334b101e4d9321b56b660d40265c1540a08ea6ccc7481701
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f77f89113321818ff8edc5976687205c8fa99744a8021370f3de6528b4179dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.6 MB (688578281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1218f1732259a9a79f0bb232898f13d0003ab6491ab743f59a808c1b3426e60b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:04:56.853519418Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T22:04:56.853519418Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20491585e2733c0a4f8f10343a305940643aa1e3523bfae1d0527d4eb5b0222`  
		Last Modified: Tue, 16 Sep 2025 17:57:40 GMT  
		Size: 4.5 MB (4493710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d00ad3e5afc4a303539c67337e65127b7ccee698dd4e0c58cab46cc14e2f0b`  
		Last Modified: Tue, 16 Sep 2025 17:57:39 GMT  
		Size: 3.5 KB (3523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5708b95ffce11f852f52583ff82769ca243573934704f55fa89f5a34652c825`  
		Last Modified: Tue, 16 Sep 2025 17:57:05 GMT  
		Size: 654.1 MB (654066462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c512ca72426db19b6b9aa188c89f314cb320b1ecb78638afceec9660dafe402e`  
		Last Modified: Tue, 16 Sep 2025 17:57:39 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ee0bb7f223f9ea17c3328dc55b4a3ca6393da44f8af06e47bca0642ae90013`  
		Last Modified: Tue, 16 Sep 2025 17:57:40 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d8f1566a0e3d2797163b520e1b1ff160f9f037700530804a03c7c2ef07f4d9`  
		Last Modified: Tue, 16 Sep 2025 17:57:40 GMT  
		Size: 163.9 KB (163930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58a79d1efa9b8ff4245effd675cdf4bbc4d79a45aa0877875ad04fb177caf04`  
		Last Modified: Tue, 16 Sep 2025 17:57:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7ba0949e8bd299c377459477e33a74c9983c24b9ee43958caeac7873cf9413`  
		Last Modified: Tue, 16 Sep 2025 17:57:41 GMT  
		Size: 115.5 KB (115527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3c576e0650f4b2b9743a557daf69f720b816f384f1b0f220a5e773acb48ecd67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eface70680383ef503cec98394941bd55ef07c34d0b0a20a89ea06421cb683dc`

```dockerfile
```

-	Layers:
	-	`sha256:e7fc19d56baa052f26dcd79a6ecb90932f2660f7ff9cbf2d3319568f58288316`  
		Last Modified: Tue, 16 Sep 2025 18:25:24 GMT  
		Size: 3.2 MB (3192742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5410712ce12f2071e430376d6316cfc800ca04d2578249c89b0f0774366e7252`  
		Last Modified: Tue, 16 Sep 2025 18:25:25 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:7473b4a37e6a80e2d66e017e208b5911e035980ec6ade735d232e20922708977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.0 MB (530992020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f71ad9ae95811fcfe50e66267a7684e7ac085b9af4c49aac50801795f7479f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:04:56.853519418Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T22:04:56.853519418Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=4ee681e2f5c63d2cd0aea062bb3a4c247ec2ffe0 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc0d3dab7863e8e1fa1f077fa529092b7d1874b39dc44bf65e4574a87d0d592`  
		Last Modified: Tue, 16 Sep 2025 17:55:42 GMT  
		Size: 4.5 MB (4498711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64eb3d21b8c3eed87d0bb92152dab86fb88f910c1439798c28617ee3e85b694`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 3.5 KB (3521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b341334c0dbe9c358fcfb12e7ece9c04042f6279c846f23a05420134456c684`  
		Last Modified: Tue, 16 Sep 2025 18:11:03 GMT  
		Size: 497.3 MB (497341325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c392b95d82d24be2be8f33ab6b9fcf42ac135d89adb86a71e5dda04d7bc88ee`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de732e2a50b036036f6841e71f6f9084d61553c573e002467e2a13605b56666a`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56449a39509be15034022fc72d405af01f8f566c81e6e206d25ebfb810b3a4b3`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 160.4 KB (160360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3385e868aaa166a6d97d3ba8eabb8694c45a9cc7c716271f842f540f7b4d6cb9`  
		Last Modified: Tue, 16 Sep 2025 17:55:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313d1791aff9dc13b30be5424b5fc53ae99dfb0614fc66075b014d61e0b523e3`  
		Last Modified: Tue, 16 Sep 2025 17:55:42 GMT  
		Size: 115.5 KB (115529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ab2600eb16e4913f050479c9c34f70461a47aa8318748869e629284f03157c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d03a8e1a0846e3275051d16ebafdce71c26209091354e18f0e2bf53a4224ee`

```dockerfile
```

-	Layers:
	-	`sha256:761ec85f7645ef167e08ee7f378db7fbf316e0c0219676c25fe7a4994da4ac5f`  
		Last Modified: Tue, 16 Sep 2025 18:25:31 GMT  
		Size: 3.2 MB (3193155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3bc4467033212c404752d8b830f8f486f933466c9a49144805dcc30f21aec9a`  
		Last Modified: Tue, 16 Sep 2025 18:25:31 GMT  
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

## `elasticsearch:9.0.7`

```console
$ docker pull elasticsearch@sha256:28a8b47e3ee14ca9bc8d8954008705243f5aff05b9896fbb9245e643f5309dd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.7` - linux; amd64

```console
$ docker pull elasticsearch@sha256:311a8dde1b35d6f12935a4d2bd61e246b081b5af305f39c169e9d09c612d3c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700688502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2920885bc160c15a41719dc076d73ddeff550a44452c26ace5ad4616b6d316`
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
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:06:39.784049935Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:06:39.784049935Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a070f035d38b12779ed27363232926dd08a077ea3f00ab4d140ccb4ce89a0`  
		Last Modified: Tue, 16 Sep 2025 17:59:39 GMT  
		Size: 4.3 MB (4284063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d462867f535bb0bf2592edf7b47a23f3dccef575593b185306abac7e0348c1b`  
		Last Modified: Tue, 16 Sep 2025 17:59:38 GMT  
		Size: 1.5 KB (1533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c93595eb43d85bb8107da186780c4e42b399d3e7525ac2955f5df9464cd708`  
		Last Modified: Tue, 16 Sep 2025 17:59:38 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc352c329947b8787ab3a9583128095717b3236fb20c4500a4eb7950d3c8795`  
		Last Modified: Tue, 16 Sep 2025 18:09:12 GMT  
		Size: 656.7 MB (656666617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a31270ae77bc6eb5f72a3c2aa27bdb4ffff8788321d559541b15a6f0e3f7a9`  
		Last Modified: Tue, 16 Sep 2025 17:59:38 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599950e348ffc48bcdb759e73de2efc32c29eb46b52b5c75afcc9d72d256716c`  
		Last Modified: Tue, 16 Sep 2025 17:59:39 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3b5d554580ae7d49d5b572611e9976464908d235a0f037787abbde5ce648d4`  
		Last Modified: Tue, 16 Sep 2025 17:59:39 GMT  
		Size: 75.8 KB (75750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510de42cd0effb01ed6c709a9ee8473b18096b58e9e6541c481ad04d8fe3956f`  
		Last Modified: Tue, 16 Sep 2025 17:59:39 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:56ae5ab5e8d98137f555c7e572aed7b088b024c98c1a20a0ab90bba88a1e8068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9102383a35d76729d54ad3d1dfd7516113516b1f0bfda19c3a4cc7c9b552cb27`

```dockerfile
```

-	Layers:
	-	`sha256:0f606ac1c331551ae649a19fbd2e019202f6d08ea26f97cb3e0901af37704140`  
		Last Modified: Tue, 16 Sep 2025 18:25:34 GMT  
		Size: 2.0 MB (2030665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1476132cc22c598078eeb7a11788de75226557fad67673e89bd57df580a61be7`  
		Last Modified: Tue, 16 Sep 2025 18:25:34 GMT  
		Size: 33.8 KB (33838 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.7` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6bdb643ffb8d90be9ee455385e035f802016bc5fe65285eee746f16e1d08a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.2 MB (539175449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3aefd8cabed36ab857a3c51f3b26d66e914d9da7f547ddb1f05745a5bc17ea3`
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
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
ENV SHELL=/bin/bash
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:06:39.784049935Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:06:39.784049935Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c6d8fb31b39450a223671e79141dd1c4b2759b5f org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["eswrapper"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a682d8d78c2251b6975141940a22482b6872cf9543f630bc2d2ce459b39051bf`  
		Last Modified: Tue, 16 Sep 2025 17:55:37 GMT  
		Size: 4.3 MB (4293026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be3a580ad7c388213cebf2eab650a35425a9c2340f92b06efea3d085f45817e`  
		Last Modified: Tue, 16 Sep 2025 17:55:36 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0a7e7034c27b1971d5d3d0ba709903d0161a571b82b15d12196418f5dffedd`  
		Last Modified: Tue, 16 Sep 2025 17:55:36 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c77751849f8eb305731b5af9a0a8e3fcdecbbca3adf94d82861bf60f84a6ab2`  
		Last Modified: Tue, 16 Sep 2025 17:54:56 GMT  
		Size: 496.9 MB (496933852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cf1c13721487d1eac85987f00f646713ae6a797ba5dd3a87f7905af07cd58b`  
		Last Modified: Tue, 16 Sep 2025 17:55:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36134aff035bc0b93de3c8c74817c4106338a0824344cc878df22af8960d631`  
		Last Modified: Tue, 16 Sep 2025 17:55:36 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee3eff57ff0369eaf86b22cbbf3183084e4a80087e79a4abdb3a47c66db04e`  
		Last Modified: Tue, 16 Sep 2025 17:55:36 GMT  
		Size: 74.6 KB (74642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68e918e207586ffa7cad54256573eab4844d4d7deb1d8c8e8d2b284c9d9ce84`  
		Last Modified: Tue, 16 Sep 2025 17:55:36 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.7` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:40e0a3f7894b8feefb92cd5ddec313263d8655b828ea511bd2f335305c45079b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0e753b5f6a91ffd9f52c1c6e38162a98a071c6114316dcf80676d0237272a7`

```dockerfile
```

-	Layers:
	-	`sha256:a27b4a647027b04e329663685322f8bf4b03ba52d3e7e4c54f81c89e45de7c2c`  
		Last Modified: Tue, 16 Sep 2025 18:25:39 GMT  
		Size: 2.0 MB (2031229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64acfb6977a8f35097daee2bcb908fcf8c33e3a3a9e847a43d4467c47d621dd5`  
		Last Modified: Tue, 16 Sep 2025 18:25:40 GMT  
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
