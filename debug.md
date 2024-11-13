[93mWARNING [0m:   FAB ID is not provided; the default ClientApp will be loaded.
[91mERROR [0m:     ServerApp thread raised an exception: Unable to load module kareem.app


The object reference string should have the form <module>:<attribute>. Valid
examples include `client:app` and `project.package.module:wrapper.app`. It must
refer to a module on the PYTHONPATH and the module needs to have the specified
attribute.

[91mERROR [0m:     An exception occurred !! module 'kareem.app' not in sys.modules
[91mERROR [0m:     Traceback (most recent call last):
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/simulation/run_simulation.py", line 378, in _main_loop
    vce.start_vce(
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/superlink/fleet/vce/vce_api.py", line 394, in start_vce
    raise ex
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/superlink/fleet/vce/vce_api.py", line 363, in start_vce
    client_app = app_fn()
                 ^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/superlink/fleet/vce/vce_api.py", line 348, in _load
    app = _get_load_client_app_fn(
          ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/client/supernode/app.py", line 239, in _load
    client_app = load_app(client_app_ref, LoadClientAppError, runtime_project_dir)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/common/object_ref.py", line 171, in load_app
    importlib.reload(m)
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/importlib/__init__.py", line 169, in reload
    _bootstrap._exec(spec, module)
  File "<frozen importlib._bootstrap>", line 606, in _exec
ImportError: module 'kareem.app' not in sys.modules

[91mERROR [0m:     Traceback (most recent call last):
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/common/object_ref.py", line 149, in load_app
    module = importlib.import_module(module_str)
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "<frozen importlib._bootstrap>", line 1204, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1176, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1147, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 690, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 940, in exec_module
  File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
  File "/home/kareem/hacking/research/AI_Love/FL_learning/kareem/kareem/app.py", line 15, in <module>
    from kareem.client_app import gen_client_fn, get_parameters
ModuleNotFoundError: No module named 'kareem.client_app'

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/simulation/run_simulation.py", line 292, in server_th_with_start_checks
    run_server_app(
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/run_serverapp.py", line 76, in run
    server_app = _load()
                 ^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/run_serverapp.py", line 63, in _load
    server_app: ServerApp = load_app(
                            ^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/common/object_ref.py", line 174, in load_app
    raise error_type(
flwr.server.server_app.LoadServerAppError: Unable to load module kareem.app


The object reference string should have the form <module>:<attribute>. Valid
examples include `client:app` and `project.package.module:wrapper.app`. It must
refer to a module on the PYTHONPATH and the module needs to have the specified
attribute.


Exception in thread Thread-1 (server_th_with_start_checks):
Traceback (most recent call last):
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/common/object_ref.py", line 149, in load_app
    module = importlib.import_module(module_str)
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "<frozen importlib._bootstrap>", line 1204, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1176, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1147, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 690, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 940, in exec_module
  File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
  File "/home/kareem/hacking/research/AI_Love/FL_learning/kareem/kareem/app.py", line 15, in <module>
    from kareem.client_app import gen_client_fn, get_parameters
ModuleNotFoundError: No module named 'kareem.client_app'

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/threading.py", line 1045, in _bootstrap_inner
    self.run()
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/threading.py", line 982, in run
    self._target(*self._args, **self._kwargs)
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/simulation/run_simulation.py", line 292, in server_th_with_start_checks
    run_server_app(
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/run_serverapp.py", line 76, in run
    server_app = _load()
                 ^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/run_serverapp.py", line 63, in _load
    server_app: ServerApp = load_app(
                            ^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/common/object_ref.py", line 174, in load_app
    raise error_type(
flwr.server.server_app.LoadServerAppError: Unable to load module kareem.app


The object reference string should have the form <module>:<attribute>. Valid
examples include `client:app` and `project.package.module:wrapper.app`. It must
refer to a module on the PYTHONPATH and the module needs to have the specified
attribute.

Traceback (most recent call last):
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/simulation/run_simulation.py", line 378, in _main_loop
    vce.start_vce(
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/superlink/fleet/vce/vce_api.py", line 394, in start_vce
    raise ex
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/superlink/fleet/vce/vce_api.py", line 363, in start_vce
    client_app = app_fn()
                 ^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/server/superlink/fleet/vce/vce_api.py", line 348, in _load
    app = _get_load_client_app_fn(
          ^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/client/supernode/app.py", line 239, in _load
    client_app = load_app(client_app_ref, LoadClientAppError, runtime_project_dir)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/common/object_ref.py", line 171, in load_app
    importlib.reload(m)
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/importlib/__init__.py", line 169, in reload
    _bootstrap._exec(spec, module)
  File "<frozen importlib._bootstrap>", line 606, in _exec
ImportError: module 'kareem.app' not in sys.modules

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/simulation/run_simulation.py", line 395, in _main_loop
    raise RuntimeError("An error was encountered. Ending simulation.") from ex
RuntimeError: An error was encountered. Ending simulation.

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "/home/kareem/mambaforge/envs/fl/bin/flower-simulation", line 8, in <module>
    sys.exit(run_simulation_from_cli())
             ^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/simulation/run_simulation.py", line 172, in run_simulation_from_cli
    _run_simulation(
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/simulation/run_simulation.py", line 569, in _run_simulation
    _main_loop(*args)
  File "/home/kareem/mambaforge/envs/fl/lib/python3.11/site-packages/flwr/simulation/run_simulation.py", line 405, in _main_loop
    raise RuntimeError("Exception in ServerApp thread")
RuntimeError: Exception in ServerApp thread

CalledProcessError: Command '['flower-simulation', '--app', '.', '--num-supernodes', '10']' returned non-zero exit status 1.
