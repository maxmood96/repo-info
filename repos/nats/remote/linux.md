## `nats:linux`

```console
$ docker pull nats@sha256:0a31000c798112718df04a19491c39f2dd8e36ba4955b8b7a9987581d5f8a033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:dbab4c53c0de6b089ceb67849d41bdf54a0ad29e50f1105048fc5f19508db803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2cbf0fba619173e5c4542920b1d7278a5a780baf2b54bff413b32cc0016433c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Sat, 16 Mar 2024 08:49:06 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:49:06 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:49:06 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:49:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5866d738de7ab782f2ba4b31cfeee8894a26c596bed7b85f7072494d10cd5618`  
		Last Modified: Sat, 16 Mar 2024 08:49:54 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:23b831c97175a24dafc1e4858d66d89b5daea7b40475fa65a5a2cc646495f69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f14c4fc39384124daeb9de82f2f548ed59cf95ac2c5163a4e7cb933758b47c6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 08:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Sat, 16 Mar 2024 08:44:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 08:44:37 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 08:44:37 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 08:44:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dcfc63d9869b797864f5925982e824e3b9ba24796e45cee98fa32eacb80c21`  
		Last Modified: Sat, 16 Mar 2024 08:45:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:d7d36063a70b3f92e87214db9cf07a81799734321a44db81a32d60f4dbe9747d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ed0bdac27116af7eb7ddd6d7e6b9ebd5fb952606a5faa4a84779b345103b0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 00:53:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 00:53:24 GMT
COPY file:6899efa16d7091375dc53de2fc1e5686e82569d9799d6cede2e40b0a8b6abb48 in /nats-server 
# Sat, 16 Mar 2024 00:53:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 00:53:25 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 00:53:25 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 00:53:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68296288971fdb3ddfe9bfba9b6a79725a69e891fb82cd5708f088afaac9929f`  
		Last Modified: Wed, 13 Mar 2024 00:36:43 GMT  
		Size: 5.3 MB (5254529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c56f0b0a93e98e48d30f323ee2f44dcffe8ee47dad4b9701cd95f33b1ad423`  
		Last Modified: Sat, 16 Mar 2024 00:54:16 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:17532cf8a200037fa12e16243b8739bc520937cd82a9a3b96d8db0e85d942071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b75af84f70f1921e86eaa7dff023270dc485b37e1acca37fe2bc3e4e919f19`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 04:04:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Sat, 16 Mar 2024 04:04:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 04:04:08 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 04:04:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3e7253e56d93fc4ce869656fef13511496d97e58250a301790645656c29acf`  
		Last Modified: Sat, 16 Mar 2024 04:04:54 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:bc4465dc1a2b2b68a903b34cd70721db4682b6ae49baad493c4fb8f9a54c1699
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123dd70806df1b073fab2d9d0cb4855270a447d3c72569af275ed24af793af46`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 02:39:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:0e1c98477f605478a27423b67d1c7bf88d4b2a56d0696ea31430a8a59b294dd8 in /nats-server 
# Sat, 16 Mar 2024 02:39:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 02:39:35 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 02:39:35 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 02:39:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7eaf17599ba122502fe00d1cb4014722df0b46a83f614f9430f71b816a6999f8`  
		Last Modified: Wed, 13 Mar 2024 01:29:44 GMT  
		Size: 5.1 MB (5096748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2405bd5e4b794b6bad044e8744cf63ddd0f2e0001abde3c0b2b5e7a190706d5e`  
		Last Modified: Sat, 16 Mar 2024 02:40:12 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:b200d259ef6d710b801ba60a7f296791ebc5298d82db48b8f68cfc0bee79d15b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26134424de3ad1af4ffe096901272e7ea3dae1a93eeddcd6c110b08b29af4011`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 16 Mar 2024 16:58:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Sat, 16 Mar 2024 16:58:41 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Sat, 16 Mar 2024 16:58:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Sat, 16 Mar 2024 16:58:43 GMT
EXPOSE 4222 6222 8222
# Sat, 16 Mar 2024 16:58:44 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 16 Mar 2024 16:58:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea5f20b9222048fdae4e26dc03a3a997375533021a900c72f4e6b338c144ddb`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
