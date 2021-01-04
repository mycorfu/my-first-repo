Git is a distributed version control system.
Git is free software distributed under the GPL
Git has a mutable index called stage.


Fixpoint eqb_list {A : Type} (eqb : A -> A -> bool)
                  (l1 l2 : list A) : bool
  (* REPLACE THIS LINE WITH ":= _your_definition_ ." *)
:=  match l1, l2 with
  | [], [] => true
  | [], a :: _ => false
  | a :: _, [] => false
  | a1 :: l1', a2 :: l2' => if eqb a1 a2 then eqb_list eqb l1' l2' else false
  end.
