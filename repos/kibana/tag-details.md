<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.6`](#kibana686)
-	[`kibana:7.5.1`](#kibana751)

## `kibana:6.8.6`

```console
$ docker pull kibana@sha256:f773d11d6a4304d1795d63b6877cf7e21bbcb4703d57444325f0a906163a408c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.6` - linux; amd64

```console
$ docker pull kibana@sha256:0a831b9e3251e777615aed743ba46ebd2b0253cd6e39c7636246515710f78379
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.9 MB (298870006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfab5632ef4cb6f1458f27dc9e580bb4c6ff04f3d219c9ddb7c92c77e312ea8`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2019 17:58:37 GMT
EXPOSE 5601
# Fri, 13 Dec 2019 17:59:22 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Fri, 13 Dec 2019 18:00:09 GMT
COPY --chown=1000:0dir:b7add46674939973162bad0e77bc7e684546e7577015c708dc2a8dad71ebd2f1 in /usr/share/kibana 
# Fri, 13 Dec 2019 18:00:10 GMT
WORKDIR /usr/share/kibana
# Fri, 13 Dec 2019 18:00:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Fri, 13 Dec 2019 18:00:13 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 13 Dec 2019 18:00:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2019 18:00:16 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Fri, 13 Dec 2019 18:00:17 GMT
COPY --chown=1000:0file:af2bc419b515a5fca0bc857249c43a0e082e6cb60c394519993854e4bc8048ca in /usr/local/bin/ 
# Fri, 13 Dec 2019 18:00:20 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Fri, 13 Dec 2019 18:00:23 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Fri, 13 Dec 2019 18:00:23 GMT
USER kibana
# Fri, 13 Dec 2019 18:00:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.6 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Fri, 13 Dec 2019 18:00:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40057de213d2c47a5d196cba4b2e8911f7caba1e0e40ddc45ff5ff1fcda7f560`  
		Last Modified: Wed, 18 Dec 2019 22:13:01 GMT  
		Size: 33.1 MB (33136094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434b62b0636c274e666fc1bc6c3577a35b48747a0bb19f61a3237bce06a61ada`  
		Last Modified: Wed, 18 Dec 2019 22:13:17 GMT  
		Size: 189.9 MB (189948389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7370972a467b446b5ca4da1b7148e5002914f5c9a4fe4e8d1a5c1cc6c3ecbcd3`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1767103506c625b66853d42b82fe0998a8db43557a61d2ed7ad5bfaedfaac4`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c66d66f9304e3a4ccfd6b61323890268da91f9253179406f2b3ece8f4c4f73`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590781aeb7f42c4f7573d916a9448a8f3acb4133bf8452c914c7c89cfed95a3f`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1efa205edea3066282cf9cd02991379b868214fce810c0260cf0fda78968056`  
		Last Modified: Wed, 18 Dec 2019 22:12:49 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.5.1`

```console
$ docker pull kibana@sha256:569a331068e399520a943cbeacf98e5a8b3b2305c6c89832c678eda4ebbd8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.5.1` - linux; amd64

```console
$ docker pull kibana@sha256:b9637bd14500a194e547cffcf1fc919d3491b5ffa605415d9e4f942c5905a5b0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.7 MB (349692840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d043e33afa466e44e9f7fa6d93597a469acfa2d4bf89de32659a72aee7a497e`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Dec 2019 00:04:24 GMT
EXPOSE 5601
# Tue, 17 Dec 2019 00:05:14 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Tue, 17 Dec 2019 00:05:16 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Tue, 17 Dec 2019 00:05:20 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Tue, 17 Dec 2019 00:05:23 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Tue, 17 Dec 2019 00:06:36 GMT
COPY --chown=1000:0dir:48b124b551a13e242d511b2c050f4d9c8ddc2b2b46bb69a8dd376baaa8744978 in /usr/share/kibana 
# Tue, 17 Dec 2019 00:06:39 GMT
WORKDIR /usr/share/kibana
# Tue, 17 Dec 2019 00:06:43 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Tue, 17 Dec 2019 00:06:43 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Dec 2019 00:06:44 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2019 00:06:45 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Tue, 17 Dec 2019 00:06:47 GMT
COPY --chown=1000:0file:23744f376b12c9d0c1869af33cd3a85883d7c67dfa3f00a276258846b6089898 in /usr/local/bin/ 
# Tue, 17 Dec 2019 00:06:51 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Tue, 17 Dec 2019 00:06:53 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Tue, 17 Dec 2019 00:06:54 GMT
USER kibana
# Tue, 17 Dec 2019 00:06:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=7.5.1 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Tue, 17 Dec 2019 00:06:54 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Tue, 17 Dec 2019 00:06:55 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e215bb30651e7c9c3cb068a2361df6ff0a3b873650b5b84799fbe984e6a466`  
		Last Modified: Wed, 18 Dec 2019 19:41:11 GMT  
		Size: 33.1 MB (33131413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6107ae08f064447d8990de296aa36e619549f3bf9f66cd655cbd713cbb937b36`  
		Last Modified: Wed, 18 Dec 2019 19:40:41 GMT  
		Size: 31.7 KB (31696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c422d40727cb47f370ac9872ea15d85f645afdf15a9f51b8b17d8c7de9d36a`  
		Last Modified: Wed, 18 Dec 2019 19:40:41 GMT  
		Size: 30.2 KB (30204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa99d3c8ec587994e88907747ab88f5b6578c131f36d3cd360c9f08ceb22bb6`  
		Last Modified: Wed, 18 Dec 2019 19:44:07 GMT  
		Size: 240.7 MB (240713758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f35274fa88ed045888adbb2c3b758c59648551fc2111b012e22e2155fd48e`  
		Last Modified: Wed, 18 Dec 2019 19:40:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b4061bcd9bbf721a15d789cc9f108ec328a71f27894dde5350788d42185676`  
		Last Modified: Wed, 18 Dec 2019 19:40:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9029ace019df38503bec42c01272dcc061dde04bb00cd57884c8a149170afe9a`  
		Last Modified: Wed, 18 Dec 2019 19:40:36 GMT  
		Size: 2.5 KB (2501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf094831f30718b4a27fc5dd3c096e0b08efdff6a7ae825c8b4205e416702377`  
		Last Modified: Wed, 18 Dec 2019 19:40:36 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0c7aa9823bebfd6fdab7b6ae73c9b801925f25217bf6a29e62ba96757d9090`  
		Last Modified: Wed, 18 Dec 2019 19:40:37 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
