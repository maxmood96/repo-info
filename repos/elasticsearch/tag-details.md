<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.7`](#elasticsearch8187)
-	[`elasticsearch:8.19.4`](#elasticsearch8194)
-	[`elasticsearch:9.0.7`](#elasticsearch907)
-	[`elasticsearch:9.1.4`](#elasticsearch914)

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
		Last Modified: Tue, 16 Sep 2025 19:01:07 GMT  
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

## `elasticsearch:8.19.4`

```console
$ docker pull elasticsearch@sha256:fc8a4ee4241b43cd52148817339aa1c8d133cd8339dae39361b7ddd2edc59548
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3c4c1b63b7deadaaae1f4e49514ac4ecb7a4a5db3e7585b52951b1819df21726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.9 MB (695883990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871d88eb73ce6b3e45ee71fe161f99de700821e7b9d425f8d026cb0c88092804`
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
# Thu, 18 Sep 2025 08:07:26 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T22:06:03.940754111Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T22:06:03.940754111Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d76ba0f156b5c8a5a8780cff62628b319904b4a59745424f2c244c9a80f7cc4`  
		Last Modified: Thu, 18 Sep 2025 18:51:12 GMT  
		Size: 5.0 MB (4962732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef5141611c306470e8605b94e5cc8b1cca5bcfa9ae8246384e790e76188ccd`  
		Last Modified: Thu, 18 Sep 2025 18:51:12 GMT  
		Size: 3.5 KB (3525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2734b339d45096a3ca3892df9556616dc7e5ecf7c0ca39d2c3606cd74938f865`  
		Last Modified: Thu, 18 Sep 2025 18:51:54 GMT  
		Size: 660.9 MB (660903143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7639518e102858853f811a93ca93be8fdf953ceb9bde947e792e8f002340d16f`  
		Last Modified: Thu, 18 Sep 2025 18:51:10 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c409e70d9358a125e945e6d9f874b98cb9488166c225f8ea67a72691d4bdfd`  
		Last Modified: Thu, 18 Sep 2025 18:51:10 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a711a3e94cb76028fb216825215eec16d18bf422e43a1911218777a3ccf3c4`  
		Last Modified: Thu, 18 Sep 2025 18:51:10 GMT  
		Size: 163.9 KB (163931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a863425b29fdbe96947223227771ee63663a00a4e964399f38534808779144b`  
		Last Modified: Thu, 18 Sep 2025 18:51:12 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92c7bdc6fc7104b2090b92413798230af10be7b12318ffdc849eb28f3d6191`  
		Last Modified: Thu, 18 Sep 2025 18:51:12 GMT  
		Size: 115.5 KB (115526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:805c963b13cc5b91ff7f84092a6468a59a48a067ffaa1290ab9b57b876956a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e266cf98561c622bb37737510c4d1395df6196f50e7fd7a87452b080df99531`

```dockerfile
```

-	Layers:
	-	`sha256:2fc8599eff1472966ed4680d97a5419ab0cbcd11dc8821cf4c04244457a61935`  
		Last Modified: Thu, 18 Sep 2025 19:00:43 GMT  
		Size: 3.2 MB (3214203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3af4c7fa5be51d842a13b8f04c650484262b700529bf41ce7a0ab6493bc97b22`  
		Last Modified: Thu, 18 Sep 2025 19:00:45 GMT  
		Size: 36.9 KB (36883 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:624c089909d130f1c88b1b08b0a6c1903027a60e5744dab5cfe4175612948694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.3 MB (538278894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c74ef144f193b8291d9ee97a3c1f14896d26421add15f7174d0fb4a8a81beb`
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
# Thu, 18 Sep 2025 08:07:26 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T22:06:03.940754111Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T22:06:03.940754111Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=aa0a7826e719b392e7782716b323c4fb8fa3b392 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ec3a3aaea2ec5b141647d738aebd08a3c2cbf875cc9d8fadbb153224db83a`  
		Last Modified: Thu, 18 Sep 2025 18:51:09 GMT  
		Size: 5.0 MB (4971714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c5fcade66826ab14a0a45919cc20b012888d89c16c66f64d9502a2f317a89`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a85b7d5ef6ff0cb4f7033f24267c602efcd9274c188627595735833d79d48f`  
		Last Modified: Thu, 18 Sep 2025 18:52:58 GMT  
		Size: 504.2 MB (504155194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a799786c50fa2e3d89d5eb5915313dbd2800c12cfaf245d1611d19b3790acea`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79ca61efb1e2c462640659610d4a1223e85d19ac817fd533a3fb2c61fad89b7`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16146084f647c3fcdfdb6e2234d5d25978ee3a85ee8da9c9702811e7f5eb79bb`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 160.4 KB (160358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff3702d9aa78de2e741074f2afef2a3cf97abd2716e02b2bdd649cf17807c7`  
		Last Modified: Thu, 18 Sep 2025 18:51:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c7bf34d618c383c9794e8495ba0f702d91a361a27d408ffe3c930ecebd0b0e`  
		Last Modified: Thu, 18 Sep 2025 18:51:06 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:b94ac2b91ddcf4591a50537207be1b89df774c31938f6ac628249d8aa1279e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f700f16d3eae18c4a80e7fd66c59ac2176d70404dd6ef306ca8896a94b3124`

```dockerfile
```

-	Layers:
	-	`sha256:cb45390f3225767c858f5af87b1be3ced2b3bfb2d81553c298b23d5f1daf6049`  
		Last Modified: Thu, 18 Sep 2025 21:25:30 GMT  
		Size: 3.2 MB (3214616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bed28de0fce04e0e2ab3a44da02610bd42339d1ae86ad769c26c2c7b9c1ddafa`  
		Last Modified: Thu, 18 Sep 2025 21:25:31 GMT  
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
		Last Modified: Tue, 16 Sep 2025 18:34:29 GMT  
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

## `elasticsearch:9.1.4`

```console
$ docker pull elasticsearch@sha256:21787a54d43334cf5530d4050da727ab37d2bda5c3112b60652f116577452182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3b4f640cb87f229c34d1cfea0415be8263b5e9367f0596c645e40c975aab697a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.7 MB (715689804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a46fd54433a4c62eafdaefef11a8738bc2e90c948fef219680a482144bbd683`
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
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T22:05:19.073893347Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T22:05:19.073893347Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e3f35a85b3c5d84a07bd1d5990a46ca09bd0b5012fef96c14cdb03b89de3ba`  
		Last Modified: Thu, 18 Sep 2025 18:55:48 GMT  
		Size: 4.3 MB (4284042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48bc7ca53222b04b2347aa9be1c23dc541dcd8e062a957940b31c991deddba6`  
		Last Modified: Thu, 18 Sep 2025 18:55:48 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f163970a300dfe41b202a334038e555967638c766618828cd78876eceb4e548d`  
		Last Modified: Thu, 18 Sep 2025 18:55:48 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df89460f764713bad31c73659a63efd55a9ad64f2943d477efb22a4fcf1b020`  
		Last Modified: Thu, 18 Sep 2025 21:31:17 GMT  
		Size: 671.7 MB (671667950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9c6cd4d7bdf4aba4e836375ae2b12f7d0a3bac24afc8ce8ac77ee506c8218`  
		Last Modified: Thu, 18 Sep 2025 18:55:48 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe290eb54912ec7f49525e2125a97bc6150c0c51398a442f546277f81664ee`  
		Last Modified: Thu, 18 Sep 2025 18:55:48 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24170d537079154ef3d0a343910d2ddf5c59765f05e296ff5767c07f682b745`  
		Last Modified: Thu, 18 Sep 2025 18:55:48 GMT  
		Size: 75.7 KB (75746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91ce2720b78c2ccf93ec734f16ad430e973c104eae0db669ca90411d38eae26`  
		Last Modified: Thu, 18 Sep 2025 18:55:50 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:4d6ee6ba6cdcb3dba0a3b4285fd59f52091d0c5278c5dadbac7909134dc0a4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2117997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a8e030747cc65f545d4df56038359624980a0e44a31d1e285bed9742b4744d`

```dockerfile
```

-	Layers:
	-	`sha256:3ab076ef074d6d22372603817895e06ebce2ba2e3a5865912c39da3af4f968fa`  
		Last Modified: Thu, 18 Sep 2025 21:25:34 GMT  
		Size: 2.1 MB (2084160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3d668100eb72231a2f22a69739902eb2744a3c355f425100db49f5f4d4136c`  
		Last Modified: Thu, 18 Sep 2025 21:25:35 GMT  
		Size: 33.8 KB (33837 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:5941149bd83023ea224537c06ff8378008ff6b6c6bc5e98945503609fb5c4e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.2 MB (554183925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5172e0bf99bc7623d225a4be10139b573bfdb10c07fe1ae66e16ab3338950889`
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
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
COPY /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
ENV SHELL=/bin/bash
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T22:05:19.073893347Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T22:05:19.073893347Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0b7fe68d2e369469ff9e9f344ab6df64ab9c5293 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Elasticsearch description=You know, for search.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["eswrapper"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb045421c1567fab441676b1a7c4048908ce39a79bf02da3556a2766914889e9`  
		Last Modified: Thu, 18 Sep 2025 18:51:49 GMT  
		Size: 4.3 MB (4293013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340d12d90e1561543136cddac959323f6907c1d65f7fb8fc93b9ea0f6c7660e7`  
		Last Modified: Thu, 18 Sep 2025 18:51:48 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2208ded6291b05e7d30ceac0438b4c7e011d4fa0a3f36345f50ad74a27bb1e0`  
		Last Modified: Thu, 18 Sep 2025 18:51:48 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2312f45461dd16d941b0cdaf8bb6af84488d809133e6348a36a6429a9e2729a4`  
		Last Modified: Thu, 18 Sep 2025 18:53:33 GMT  
		Size: 511.9 MB (511942346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95458faa74f8531a0bfb76fa60e1227f94e3093bdd838eeb7483bd5be4d19432`  
		Last Modified: Thu, 18 Sep 2025 18:51:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dcd0d52c62a6377ba35da2ca6866d66609c14cd0e65ac85f14e97ec82bec96`  
		Last Modified: Thu, 18 Sep 2025 18:51:46 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde3e7bddec442c41f618fc1f1a6455bae4b04bef4a8bb62090600a7a1dbe76c`  
		Last Modified: Thu, 18 Sep 2025 18:51:46 GMT  
		Size: 74.6 KB (74638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c43fd12ce3a7bdc444d4d77666cfd70b18e9e08aceaaf0ea788a6fc3b58ffd`  
		Last Modified: Thu, 18 Sep 2025 18:51:46 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a9727740c0878fd86256e743278d81d13f0b6bc4b8622293ec6b2083bad3a59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1413e65ba43021dc015dd0e1afd9758e063459185419a927e18b5ff70e8f9a`

```dockerfile
```

-	Layers:
	-	`sha256:c77fbe76fd626ab267b90d1f11ae054606c54d11b09cfd429d6c7a995ee60293`  
		Last Modified: Thu, 18 Sep 2025 21:25:40 GMT  
		Size: 2.1 MB (2084724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68796a50aac4b125fa4a692ed0cb5b0f4197861d06c2c1a6ed9d794c122bdfcf`  
		Last Modified: Thu, 18 Sep 2025 21:25:40 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
