## `nats:scratch`

```console
$ docker pull nats@sha256:fa099e44e96c34940a98847306fd5e812bd3fb18bca191d15cce57f7b707aadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:6fb1a85021a8411e0470cca8a43d461db915d2df605657389c4f0595d2e42e91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8780d448219e4996eb219326ba6943b7e05f04ab1189a6f1dcf2e013058e3e36`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:33d3e4ce6e17dc907ca0b478996354d26d433431b7bf48ae5bef3ec2ea1359f1 in /nats-server 
# Wed, 13 Mar 2024 01:47:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:47:57 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:47:57 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:47:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ce8539fabe7af34129953a073c64515d008d19eac52a820ef52368f6411e540d`  
		Last Modified: Wed, 13 Mar 2024 01:48:46 GMT  
		Size: 5.5 MB (5547633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5208dae10516783bd9b5be071d7f3d39c84e1138b3887856c85f570ec4f588c`  
		Last Modified: Wed, 13 Mar 2024 01:48:45 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:b717fb731a88e81bdabf9b7eb28e2ee0fa423ff801dcd5819fb4ffaf217cb208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51552a7d22c2c5ca2447ff2b4198de16cfdff9a116a3c54ef5af0d997a9469f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:c24c6855bab6e8b64a222738f44249dd58afe5ec56a34cfd64493e736f5325df in /nats-server 
# Wed, 13 Mar 2024 00:49:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:49:35 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:49:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:bc2b5fa4421ea8f446fd52c0a8e7c8c6e048dc4aa6a096fb60765aa281147267`  
		Last Modified: Wed, 13 Mar 2024 00:50:20 GMT  
		Size: 5.3 MB (5263253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652cf78472b592b1ea355485d1a353340ba41c0d01b26f15ffacc090db84d7bb`  
		Last Modified: Wed, 13 Mar 2024 00:50:19 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

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

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f8017338e2c0dd9d3adb17672dd8226d475d5c810fa5f742c27a1d77f6e0c0e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8216507954fc8ffbaa79f3aa0908756fb3b5e699a13215671cf23837d30ca343`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:674069719b01a345db55aa1ea35485a8b6f0cf0eed465ae05a0c00073e2ab2ab in /nats-server 
# Wed, 13 Mar 2024 00:40:40 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 00:40:40 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 00:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d5466aeaf1139b432e415e6412234c167a91220e74d17f50be1a2de5b0fb1b21`  
		Last Modified: Wed, 13 Mar 2024 00:41:26 GMT  
		Size: 5.1 MB (5117178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c0bd40d1b70ec911e4b7219f7867675e2ad1c67899a3643f13d261d792187`  
		Last Modified: Wed, 13 Mar 2024 00:41:25 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

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

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:21d23f9777f88070c60ce8bf669dd9169ad10d91ddae1f43c02b5419cc5fcbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9daecac5ba461be180b94ca61fe053ebe1e5c23af8e61522f1854982e6157`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 11 Jan 2024 17:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:cc94c349de0e266f428d63773845fb669334304c5fbcffeec57553d333126f22 in /nats-server 
# Wed, 13 Mar 2024 01:15:09 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 13 Mar 2024 01:15:09 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:15:09 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 13 Mar 2024 01:15:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0bf838b872f1e012c580bbff8d1e66a09a7b05a85651db222851ea3323dab3d2`  
		Last Modified: Wed, 13 Mar 2024 01:16:47 GMT  
		Size: 5.4 MB (5430321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668de88817078f4ef2cf284dff428f40567f94b7132efee56fe3abe6264e6d42`  
		Last Modified: Wed, 13 Mar 2024 01:16:46 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
