# sinan_auto

## 환경 설정
1. ubuntu 22.04
2. 서버 1 : GPU 사용 서버 2 : 무관
3. sinan 수정 사항
'''
cluster configuration
sinan-local/docker_swarm/misc/ make_cluster_config.py L46-47, L108-121
실행 명령어 : python3 make_cluster_config.py --nodes oslab oslab2 --cluster-config test_cluster.json --replica-cpus 4
engine configuration
sinan-local/docker_swarm/misc/make_gpu_config.py L31-L34
Data collection
docker_swarm/scripts/run_data_collect.sh -> run_data_collect_sy.sh 실행
Failed to construct tracer 문제 해결
sinan-local/benchmarks/socialNetwork-ml-swarm/nginx-web-server/jaeger-config.json 
"localAgentHostPort": "jaeger:6831"
media error -> benchmark 및 media 경로 변경
sinan-local/benchmarks/socialNetwork-ml-swarm/scripts/
debug_compose_short_post_sync.py L122-123
setup_social_graph_init_data.py L122-123
test_compose_post_sync.py L122-123
test_compose_short_post_sync.py L122-123
bechmarks 경로 변경
sinan-local/benchmarks/socialNetwork-ml-swarm/wrk2/scripts/social-network/
compose-post.lua L45
mixed-workload.lua L37  
'''

